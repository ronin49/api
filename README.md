5157b37b-e47b-42f5-bcc9-ea401f1e1937



ATCTT3xFfGN0wp32iIVt3rfJVj6l0SY7eSZoy3moXIuS-7O3ItrAJEJ_sg3quG7ntMvX6WgPv0Qv44GJ5nFPWnTlnDsLJ4A0Xns9rFKI8NNlp1437H6BJPEWOoC24vKXpovaVdpfW-96zIAis65t0a4cZBQqkhN7kzWRVed2zlX-nX2OPXbi_ws=E58937A2



ATATT3xFfGF0MEBw7CpVeKxR9qjnDUPUk7osO1gJG8gCH0GcKEROHJNZwrbdKG_YNlc0N0Jt50JCh3SpnpzoqnjnnGcDmpD4rvmYbCp4qnJO8YYrdSDqHHHQVJBVlB0M34rJw6nZrVjFkM36Xeq97LWXBApPugXMHwMG6b1qqiWXL21MQVtVxh0=9E0A8FD2




namespace py estimator

struct Issue {
  1: string key
  2: string summary
  3: string description
  4: string issueType
}

struct EstimationResult {
  1: i32 storyPoints
  2: string reasoning
}

service StoryPointEstimator {
  EstimationResult estimate(1: Issue issue)
}



import { fetch } from '@forge/api';

export async function run() {
  const response = await fetch('https://api.example.com/data', {
    method: 'GET',
    headers: {
      'Accept': 'application/json'
    }
  });

  if (!response.ok) {
    return {
      body: `Request failed: ${response.status}`
    };
  }

  const data = await response.json();

  return {
    body: `Response from server: ${JSON.stringify(data)}`
  };
}
