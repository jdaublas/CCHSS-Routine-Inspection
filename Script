function handleBranching(selectId, detailsDivId) {
  const select = document.getElementById(selectId);
  const detailsDiv = document.getElementById(detailsDivId);

  select.addEventListener('change', function() {
    if (["No","Partially","Somewhat","Rarely"].includes(select.value)) {
      detailsDiv.classList.remove('hidden');
      detailsDiv.querySelector('textarea').required = true;
    } else {
      detailsDiv.classList.add('hidden');
      detailsDiv.querySelector('textarea').required = false;
    }
  });
}

handleBranching('serviceReview', 'serviceReviewDetailsDiv');
handleBranching('governanceStructure', 'governanceStructureDetailsDiv');
handleBranching('policyAwareness', 'policyAwarenessDetailsDiv');
handleBranching('trainingReceived', 'trainingNeededDetailsDiv');
handleBranching('safetyProtocols', 'safetyProtocolsDetailsDiv');

document.getElementById('cchssForm').addEventListener('submit', function(e) {
  e.preventDefault();
  const formData = new FormData(this);
  const data = {};
  formData.forEach((value, key) => { data[key] = value });
  console.log("Survey Responses:", data);
  alert("Thank you! Your responses have been submitted.");
  this.reset();
  document.querySelectorAll('.hidden').forEach(div => div.classList.add('hidden'));
});
