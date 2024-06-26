{% from "common/macros.njk" import get_date with context %}

{% set weekly_tp_tasks = {
week2: [
  {id: 'get_familiar_with_ab3'}
],
week3: [
  {id: 'start_project_notes', deadline: 'before the next lecture'},
  {id: 'decide_project_direction', deadline: 'before the next lecture'}
],
week4: [
  {id: 'brainstorm_user_stories'},
  {id: 'prioritize_user_stories'}
],
week5: [
  {id: 'conceptualize_first_version'},
  {id: 'draft_the_ug'},
  {id: 'refine_product_design'},
  {id: 'set_up_project_repo'},
  {id: 'get_familiar_with_the_code_base'}
],
week6: [
  {id: 'do_a_practice_iteration'},
  {id: 'update_website_aboutus_readme'},
  {id: 'update_the_ug'},
  {id: 'update_dg_user_stories_etc'},
  {id: 'plan_the_next_iteration'},
  {id: 'start_implementing_the_next_version'}
],
week7: [
  {id: 'ensure_you_know_tp_expectations'},
  {id: 'start_proper_milestone_management'},
  {id: 'add_first_functionality_increment'}
],
week8: [
  {id: 'deliver_first_version'},
  {id: 'wrap_up_first_version'},
  {id: 'do_an_informal_demo'}
],
week9: [
  {id: 'do_a_postmortem'},
  {id: 'adjust_process_rigor'},
  {id: 'start_on_the_penultimate_version'},
  {id: 'update_dg_with_design_details'}
],
week10: [
  {id: 'wrap_up_penultimate_version'}
],
week11: [
  {id: 'alpha_test'}
],
week12: [
  {id: 'draft_the_ppp'},
  {id: 'make_code_reposense_compatible'},
  {id: 'do_final_tweaks'},
  {id: 'prepare_final_deliverables'}
],
week13: [
  {id: 'submit_final_deliverables', deadline: get_date(date_final_submission)},
  {id: 'wrap_up_final_milestone', deadline: get_date(date_final_submission, 2)},
  {id: 'demo_the_product', deadline: get_date(date_final_submission, 2)}
]
} %}

{% set weekly_tp_themes = {
  w2: {name: "Kickoff"},
  w3: {name: "Set direction"},
  w4: {name: "Gather requirements"},
  w5: {name: "Conceptualize the product"},
  w6: {name: "Get ready for iterations", milestone: version_practice},
  w7: {name: "mid-" + version_mvp},
  w8: {name: version_mvp, milestone: version_mvp},
  w9: {name: "mid-" + version_penultimate},
  w10: {name: version_penultimate, milestone: version_penultimate},
  w11: {name: "mid-" + version_final},
  w12: {name: "final tweaks"},
  w13: {name: version_final, milestone: version_final}
} %}
