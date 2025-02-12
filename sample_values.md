INSERT INTO user (user_id, username, password, email, registration_date) VALUES
(11, 'tanmay_92', 'tanmaypass', 'tanmay@example.com', '2024-03-18'),
(12, 'siddhant_singh', 'siddhant123', 'siddhant@example.com', '2024-03-18'),
(13, 'aditi_gupta', 'aditipass', 'aditi@example.com', '2024-03-18'),
(14, 'rachit_84', 'rachitpass', 'rachit@example.com', '2024-03-18'),
(15, 'navinya_sharma', 'navinyapass', 'navinya@example.com', '2024-03-18'),
(16, 'prerit_07', 'preritpass', 'prerit@example.com', '2024-03-18'),
(17, 'khushal_99', 'khushalpass', 'khushal@example.com', '2024-03-18'),
(18, 'elon_musk', 'spacex123', 'elon.musk@example.com', '2024-03-18'),
(19, 'elwish_88', 'elwishpass', 'elwish@example.com', '2024-03-18');

INSERT INTO profile (profile_id, user_id, first_name, last_name, bio, birth_date, picture) VALUES
(1, 11, 'Tanmay', 'Sharma', 'Software Engineer with a passion for coding.', '1992-05-15', 'tanmay.jpg'),
(2, 12, 'Siddhant', 'Singh', 'Aspiring entrepreneur exploring new opportunities.', '1995-09-20', 'siddhant.jpg'),
(3, 13, 'Aditi', 'Gupta', 'Travel enthusiast and avid reader.', '1990-12-10', 'aditi.jpg'),
(4, 14, 'Rachit', 'Kumar', 'Tech enthusiast and blogger.', '1994-03-28', 'rachit.jpg'),
(5, 15, 'Navinya', 'Sharma', 'Passionate artist and animal lover.', '1993-07-17', 'navinya.jpg'),
(6, 16, 'Prerit', 'Jain', 'Fitness enthusiast and motivational speaker.', '1997-01-05', 'prerit.jpg'),
(7, 17, 'Khushal', 'Patel', 'Foodie and aspiring chef.', '1998-11-22', 'khushal.jpg'),
(8, 18, 'Elon', 'Musk', 'Visionary entrepreneur and CEO of SpaceX and Tesla.', '1971-06-28', 'elon.jpg'),
(9, 19, 'Elwish', 'Kaur', 'Fashion designer and blogger.', '1990-08-18', 'elwish.jpg');

INSERT INTO tweet (tweet_id, user_id, tweet_text, timestamp, likes, retweets) VALUES
(1, 11, 'Just finished coding a new feature! #CodingLife', '2024-03-18 10:30:00', 20, 5),
(2, 12, 'Excited to launch my new startup next month! #Entrepreneurship', '2024-03-18 11:45:00', 15, 3),
(3, 13, 'Just returned from a fantastic trip to the mountains! #TravelDiaries', '2024-03-18 12:15:00', 30, 10),
(4, 14, 'Published a new blog post on the latest tech trends. Check it out! #Tech', '2024-03-18 13:20:00', 25, 8),
(5, 15, 'Completed a new painting today. Feeling inspired! #Art', '2024-03-18 14:00:00', 40, 12),
(6, 16, 'Push your limits and never give up! #Motivation', '2024-03-18 15:30:00', 50, 15),
(7, 17, 'Experimenting with new recipes in the kitchen today. #Foodie', '2024-03-18 16:45:00', 35, 6),
(8, 18, 'Mars colonization is the future! #SpaceX #Mars', '2024-03-18 17:10:00', 100, 50),
(9, 19, 'New fashion trends for the upcoming season. Stay tuned! #Fashion', '2024-03-18 18:20:00', 45, 20);

INSERT INTO comment (comment_id, tweet_id, user_id, comment_text, timestamp) VALUES
(1, 1, 12, 'Great job, Tanmay!', '2024-03-18 10:35:00'),
(2, 2, 13, 'Looking forward to it, Siddhant!', '2024-03-18 11:50:00'),
(3, 3, 14, 'Wow, Aditi! That sounds amazing.', '2024-03-18 12:20:00'),
(4, 4, 15, 'Rachit, your blog posts are always insightful.', '2024-03-18 13:25:00'),
(5, 5, 16, 'Navinya, your paintings are so beautiful!', '2024-03-18 14:05:00'),
(6, 6, 17, 'Thanks for the motivation, Prerit!', '2024-03-18 15:35:00'),
(7, 7, 18, 'I am a big fan of your work, Elon!', '2024-03-18 16:50:00'),
(8, 8, 19, 'Agreed! Mars colonization will change everything.', '2024-03-18 17:15:00'),
(9, 9, 11, 'Excited to see the new fashion trends, Elwish!', '2024-03-18 18:25:00');

INSERT INTO followers (followerID, followerUserID, followingUserID) VALUES
(1, 11, 12),
(2, 12, 13),
(3, 13, 14),
(4, 14, 15),
(5, 15, 16),
(6, 16, 17),
(7, 17, 18),
(8, 18, 19),
(9, 19, 11),
(10, 11, 14),
(11, 11, 15),
(12, 11, 16),
(13, 11, 17);

INSERT INTO hashtag (hashtag_id, hashtag_text) VALUES
(1, 'CodingLife'),
(2, 'Entrepreneurship'),
(3, 'TravelDiaries'),
(4, 'Tech'),
(5, 'Art'),
(6, 'Motivation'),
(7, 'Foodie'),
(8, 'SpaceX'),
(9, 'Fashion');

INSERT INTO tweethashtag (tweethashtag_id, tweet_id, hashtag_id) VALUES
(1, 1, 1),
(2, 2, 2),
(3, 3, 3),
(4, 4, 4),
(5, 5, 5),
(6, 6, 6),
(7, 7, 7),
(8, 8, 8),
(9, 9, 9),
(10, 1, 4),
(11, 2, 6),
(12, 3, 7),
(13, 4, 1),
(14, 5, 2),
(15, 6, 3),
(16, 7, 4),
(17, 8, 5),
(18, 9, 6);

INSERT INTO mention (mention_id, tweet_id, mentioneduser_id) VALUES
(1, 1, 12),
(2, 2, 13),
(3, 3, 14),
(4, 4, 15),
(5, 5, 16),
(6, 6, 17),
(7, 7, 18),
(8, 8, 19),
(9, 9, 11),
(10, 1, 14),
(11, 2, 15),
(12, 3, 16),
(13, 4, 17),
(14, 5, 18),
(15, 6, 19),
(16, 7, 11),
(17, 8, 12),
(18, 9, 13);

INSERT INTO notification (notification_id, user_id, notification_text, timestamp, is_read) VALUES
(1, 11, 'You have a new follower!', '2024-03-18 10:30:00', false),
(2, 12, 'Your tweet has been liked!', '2024-03-18 11:45:00', true),
(3, 13, 'You have been mentioned in a tweet!', '2024-03-18 12:15:00', false),
(4, 14, 'New message received!', '2024-03-18 13:20:00', false),
(5, 15, 'Your tweet has been retweeted!', '2024-03-18 14:00:00', true),
(6, 16, 'You have a new follower!', '2024-03-18 15:30:00', false),
(7, 17, 'Your tweet has been liked!', '2024-03-18 16:45:00', false),
(8, 18, 'You have been mentioned in a tweet!', '2024-03-18 17:10:00', true),
(9, 19, 'New message received!', '2024-03-18 18:20:00', false);

INSERT INTO message (message_id, senderuser_id, receiveruser_id, message_text, timestamp, is_read) VALUES
(1, 11, 12, 'Hey, how are you?', '2024-03-18 10:30:00', true),
(2, 12, 13, 'Did you see the latest news?', '2024-03-18 11:45:00', false),
(3, 13, 14, 'Lets catch up sometime!', '2024-03-18 12:15:00', false),
(4, 14, 15, 'Thanks for the update!', '2024-03-18 13:20:00', true),
(5, 15, 16, 'Are you coming to the party?', '2024-03-18 14:00:00', false),
(6, 16, 17, 'Check out this cool article!', '2024-03-18 15:30:00', true),
(7, 17, 18, 'Can you help me with this?', '2024-03-18 16:45:00', true),
(8, 18, 19, 'Lets plan our next trip!', '2024-03-18 17:10:00', false),
(9, 19, 11, 'Remember to buy groceries!', '2024-03-18 18:20:00', false);

INSERT INTO group_name (group_id, group_name, admin_id) VALUES
(1, 'Tech Enthusiasts', 11),
(2, 'Travel Lovers', 13),
(3, 'Fitness Freaks', 16);

INSERT INTO groupmembers (groupmember_id, group_id, user_id) VALUES
(1, 1, 11),  
(2, 1, 14),  
(3, 2, 13),  
(4, 2, 15),  
(5, 3, 16),  
(6, 3, 17),  
(7, 1, 12),  
(8, 2, 11),  
(9, 3, 19);  

INSERT INTO poll (poll_id, tweet_id, question, expirydate) VALUES
(1, 1, 'Which programming language do you prefer?', '2024-03-25'),
(2, 2, 'Where is your dream travel destination?', '2024-04-01'),
(3, 3, 'How often do you exercise?', '2024-03-28');

INSERT INTO polloption (option_id, poll_id, option_text, votes) VALUES
(1, 1, 'Python', 0),
(2, 1, 'JavaScript', 0),
(3, 1, 'Java', 0),
(4, 2, 'Paris', 0),
(5, 2, 'Tokyo', 0),
(6, 2, 'Bora Bora', 0),
(7, 3, 'Every day', 0),
(8, 3, '2-3 times a week', 0),
(9, 3, 'Once a week', 0);

INSERT INTO savedtweets (savedtweet_id, user_id, tweet_id) VALUES
(1, 11, 1),
(2, 12, 2),
(3, 13, 3),
(4, 14, 4),
(5, 15, 5),
(6, 16, 6),
(7, 17, 7),
(8, 18, 8),
(9, 19, 9);

INSERT INTO BlockedUsers (block_id, blockinguser_id, blockeduser_id) VALUES
(1, 11, 12),
(2, 13, 14),
(3, 15, 16),
(4, 17, 18),
(5, 19, 11),
(6, 12, 13),
(7, 14, 15),
(8, 16, 17),
(9, 18, 19);


