# DBMS
twitter_clone

User Table

CREATE TABLE user (
    user_id INT PRIMARY KEY,
    username VARCHAR(30) UNIQUE NOT NULL,
    password VARCHAR(20),
    email VARCHAR(60) UNIQUE NOT NULL ,
    registration_date DATE
);

Profile Table

CREATE TABLE profile (
    profile_id INT PRIMARY KEY,
    user_id INT,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    bio TEXT,
    birth_date DATE,
    picture VARCHAR(255),
    FOREIGN KEY (user_id) REFERENCES user(user_id)
);

Tweet Table

CREATE TABLE tweet (
    tweet_id INT PRIMARY KEY,
    user_id INT,
    tweet_text TEXT,
    timestamp TIMESTAMP,
    likes INT,
    retweets INT,
    FOREIGN KEY (user_id) REFERENCES user(user_id)
);

Comment Table

CREATE TABLE comment (
    comment_id INT PRIMARY KEY,
    tweet_id INT,
    user_id INT,
    comment_text TEXT,
    timestamp TIMESTAMP,
    FOREIGN KEY (tweet_id) REFERENCES tweet(tweet_id),
    FOREIGN KEY (user_id) REFERENCES user(user_id)
);

Followers Table

CREATE TABLE followers (
    followerID INT PRIMARY KEY,
    followerUserID INT,
    followingUserID INT,
    FOREIGN KEY (followerUserID) REFERENCES user(user_id),
    FOREIGN KEY (followingUserID) REFERENCES user(user_id)
);

Hashtag Table

CREATE TABLE hashtag (
    hashtag_id INT PRIMARY KEY,
    hashtag_text VARCHAR(100)
);

TweetHashtag Table

CREATE TABLE tweethashtag (
    tweethashtag_id INT PRIMARY KEY,
    tweet_id INT,
    hashtag_id INT,
    FOREIGN KEY (tweet_id) REFERENCES tweet(tweet_id),
    FOREIGN KEY (hashtag_id) REFERENCES hashtag(hashtag_id)
);

Mentions Table

CREATE TABLE mention (
    mention_id INT PRIMARY KEY,
    tweet_id INT,
    mentioneduser_id INT,
    FOREIGN KEY (tweet_id) REFERENCES tweet(tweet_id),
    FOREIGN KEY (mentioneduser_id) REFERENCES user(user_id)
);

Notification Table

CREATE TABLE notification (
    notification_id INT PRIMARY KEY,
    user_id INT,
    notification_text TEXT,
    timestamp TIMESTAMP,
    is_read BOOLEAN,
    FOREIGN KEY (UserID) REFERENCES user(UserID)
);

Message Table

CREATE TABLE message (
    message_id INT PRIMARY KEY,
    senderuser_id INT,
    receiveruser_id INT,
    message_text TEXT,
    timestamp TIMESTAMP,
    is_read BOOLEAN,
    FOREIGN KEY (senderuser_id) REFERENCES user(user_id),
    FOREIGN KEY (receiveruser_id) REFERENCES user(user_id)
);

Group Table

CREATE TABLE group (
    group_id INT PRIMARY KEY,
    group_name VARCHAR(255),
    admin_id INT,
    FOREIGN KEY (admin_id) REFERENCES user(user_Id)
);

GroupMembers Table

CREATE TABLE groupmembers (
    groupmember_id INT PRIMARY KEY,
    group_id INT,
    user_id INT,
    FOREIGN KEY (group_id) REFERENCES group(group_id),
    FOREIGN KEY (user_id) REFERENCES user(user_id)
);

Poll Table

CREATE TABLE poll (
    poll_id INT PRIMARY KEY,
    tweet_id INT,
    question TEXT,
    expirydate DATE,
    FOREIGN KEY (tweet_id) REFERENCES tweet(tweet_id)
);

PollOption Table

CREATE TABLE polloption (
    option_id INT PRIMARY KEY,
    poll_id INT,
    option_text TEXT,
    votes INT,
    FOREIGN KEY (poll_id) REFERENCES poll(poll_id)
);

SavedTweets Table

CREATE TABLE savedtweets (
    savedtweet_id INT PRIMARY KEY,
    user_id INT,
    tweet_id INT,
    FOREIGN KEY (user_id) REFERENCES user(user_id),
    FOREIGN KEY (tweet_id) REFERENCES tweet(tweet_id)
);

BlockedUsers Table

CREATE TABLE BlockedUsers (
    block_id INT PRIMARY KEY,
    blockinguser_id INT,
    blockeduser_id INT,
    FOREIGN KEY (blockinguser_id) REFERENCES user(user_id),
    FOREIGN KEY (blockeduser_id) REFERENCES user(user_id)
);
