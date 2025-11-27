[GitHub GraphQL API 설명서](https://docs.github.com/ko/graphql)

GraphQL API는 각 쿼리에 포인트를 할당하고 특정 시간 내에 사용할 수 있는 포인트를 제한합니다. 이 제한은 남용 및 서비스 거부 공격을 방지하고 모든 사용자가 API를 계속 사용할 수 있도록 합니다.

시간당 5,000포인트 :  personal access token을(를) 사용한 요청 + GitHub App 또는 OAuth app의 요청이 포함

GitHub Actions 워크플로에서 GITHUB_TOKEN의 경우: 리포지토리당 시간당 1,000포인트 GitHub.com에서 엔터프라이즈 계정에 속한 리소스에 대한 요청의 경우 리포지토리당 시간당 15,000포인트로 제한됩니다.

rateLimit 개체를 쿼리하여 트래픽률 제한을 확인할 수도 있습니다. 가능하면 API를 쿼리하는 대신 트래픽률 제한 응답 헤더를 사용하여 트래픽률 제한을 확인하는 것이 좋습니다.
필드	설명
limit    	  시간당 사용할 수 있는 최대 포인트 수
remaining  	현재 트래픽률 제한 창의 잔여 포인트 수
used	      현재 트래픽률 제한 창에서 사용한 포인트 수
resetAt	    현재 트래픽률 제한 창이 UTC Epoch 초 단위로 재설정되는 시간
