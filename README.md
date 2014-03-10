
ณัฐนันท์ ประพันธ์ศิริ 5310613194
อภิรักษ์  โชคดีวนิชวัฒนา 5310612352


<pre>
Grading:
Test passed. (+0.2)
--------------------------------------------------------------------------------
Test passed. (+0.075)
--------------------------------------------------------------------------------
Test passed. (+0.075)
--------------------------------------------------------------------------------
The following required failures were not detected:
 - restrict to movies with 'PG' or 'R' ratings
with the following modifications:
 - results = [G, PG, PG-13, R] movies
| Disabling profiles...
| Disabling profiles...
| #???????????????????????? ???????????????????????????????????? 5310613194
| # ????????????????????????  ?????????????????????????????????????????? 5310612352
| Feature: display list of movies filtered by MPAA rating
|   
|   As a concerned parent
|   So that I can quickly browse movies appropriate for my family
|   I want to see movies matching only certain MPAA ratings
| 
|   Background: movies have been added to database # /tmp/submission20140310-15273-14pp795/features/filter_movie_list.feature:10
|     Given the following movies exist:            # /tmp/submission20140310-15273-14pp795/features/step_definitions/movie_steps.rb:8
|       | title                   | rating | release_date |
|       | Aladdin                 | G      | 25-Nov-1992  |
|       | The Terminator          | R      | 26-Oct-1984  |
|       | When Harry Met Sally    | R      | 21-Jul-1989  |
|       | The Help                | PG-13  | 10-Aug-2011  |
|       | Chocolat                | PG-13  | 5-Jan-2001   |
|       | Amelie                  | R      | 25-Apr-2001  |
|       | 2001: A Space Odyssey   | G      | 6-Apr-1968   |
|       | The Incredibles         | PG     | 5-Nov-2004   |
|       | Raiders of the Lost Ark | PG     | 12-Jun-1981  |
|       | Chicken Run             | G      | 21-Jun-2000  |
|     And I am on the RottenPotatoes home page     # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:49
| 
|   Scenario: restrict to movies with 'PG' or 'R' ratings # /tmp/submission20140310-15273-14pp795/features/filter_movie_list.feature:27
|     Given I check the following ratings: PG, R          # /tmp/submission20140310-15273-14pp795/features/step_definitions/movie_steps.rb:31
|     When I uncheck the following ratings: PG-13, G      # /tmp/submission20140310-15273-14pp795/features/step_definitions/movie_steps.rb:31
|     And I press "ratings_submit"                        # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:57
|     Then I should be on the home page                   # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:235
|     Then I should see "Amelie"                          # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:110
|     Then I should see "Raiders of the Lost Ark"         # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:110
|     Then I should see "The Incredibles"                 # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:110
|     Then I should see "The Terminator"                  # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:110
|     Then I should see "When Harry Met Sally"            # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:110
|     And I should not see "The Help"                     # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:128
|     And I should not see "Chocolat"                     # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:128
|     And I should not see "Aladdin"                      # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:128
|     And I should not see "2001: A Space Odyssey"        # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:128
|     And I should not see "Chicken Run"                  # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:128
| 
|   # enter step(s) to check the 'PG' and 'R' checkboxes
|   # enter step(s) to uncheck all other checkboxes
|   # enter step to "submit" the search form on the homepage
|   # enter step(s) to ensure that PG and R movies are visible
|   # enter step(s) to ensure that other movies are not visible
|   Scenario: all ratings selected                        # /tmp/submission20140310-15273-14pp795/features/filter_movie_list.feature:49
|     When I check the following ratings: PG, R, G, PG-13 # /tmp/submission20140310-15273-14pp795/features/step_definitions/movie_steps.rb:31
|     Then I press "ratings_submit"                       # /tmp/submission20140310-15273-14pp795/features/step_definitions/web_steps.rb:57
|     Then I should see all of the movies                 # /tmp/submission20140310-15273-14pp795/features/step_definitions/movie_steps.rb:37
| 
| 2 scenarios (2 passed)
| 21 steps (21 passed)
| 0m0.871s
Test failed. (-0.075)
--------------------------------------------------------------------------------
Test passed. (+0.075)
--------------------------------------------------------------------------------
Test passed. (+0.25)
--------------------------------------------------------------------------------
Test passed. (+0.25)
Total score: 0.925 / 1.0

Total: 277.5
Late: 0
Deduction: 0
Final Score: 277.5/300
</pre>