---

copyright:

  years: 2017

lastupdated: "2017-11-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# IAM 액세스 관리
{: #iammanidaccser}

액세스를 관리하거나 사용자에 대해 새 액세스를 지정하려면 계정 소유자, 계정의 모든 서비스에 대한 관리자 또는 특정 서비스나 서비스 인스턴스에 대한 지정된 관리자여야 합니다. 정책 및 역할 액세스에 대한 자세한 정보는 [IAM 액세스](/docs/iam/users_roles.html)를 참조하십시오. 

## 기존 액세스 권한 편집

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스**를 클릭한 후에 **사용자**를 선택하십시오. 
2. 액세스를 지정할 사용자의 이름을 선택하십시오. 
3. 편집할 정책에 대한 행에서 **조치** 메뉴를 선택한 다음 **정책 편집**을 클릭하십시오.
4. 정책을 편집하십시오.
5. **저장**을 클릭하십시오.

## 새 액세스 지정
{: #assignaccess}

### 리소스 그룹 내의 리소스에 액세스 

리소스 그룹의 모든 리소스에 대해 또는 리소스 그룹 내의 하나의 서비스에 대해서만 액세스를 지정하려면 다음 단계를 완료하십시오. 

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스**를 클릭한 후에 **사용자**를 선택하십시오. 
2. 액세스를 지정할 사용자에 대한 행에서 **조치** 메뉴를 선택한 후에 **액세스 지정**을 클릭하십시오. 
3. **리소스 그룹 내의 액세스 지정**을 선택하십시오. 
4. 리소스 그룹을 선택하십시오.
5. 사용자가 대시보드에서 리소스 그룹을 보고 리소스 그룹 이름을 편집하며 그룹에 대한 사용자 액세스를 관리할 수 있도록 **리소스 그룹에 대한 액세스 지정** 필드에 대한 역할을 선택하십시오. 사용자가 지정된 리소스에만 액세스하고 리소스가 속한 그룹에는 액세스하지 못하도록 하려면 **액세스 없음**을 선택할 수 있습니다. 
6. 리소스 그룹 내의 서비스를 선택하거나, 선택된 그룹 내의 모든 서비스에 대한 액세스 제공을 선택하십시오. 
7. 사용자에 대해 원하는 액세스를 지정하기 위한 역할의 임의의 조합을 선택하십시오. 이 액세스는 정책에 대해 선택된 리소스에만 적용됩니다. 이는 리소스 그룹인 실제 컨테이너에 대한 액세스는 제공하지 않습니다. 
8. **지정**을 클릭하십시오.

### 리소스에 액세스
{: #resourceaccess}

계정의 개별 리소스에 대한 액세스 또는 계정의 모든 리소스에 대한 액세스를 지정하려면 다음 단계를 완료하십시오.  

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스**를 클릭한 후에 **사용자**를 선택하십시오. 
2. 액세스를 지정할 사용자에 대한 행에서 **조치** 메뉴를 선택한 후에 **액세스 지정**을 클릭하십시오. 
3. **리소스에 대한 액세스 지정**을 선택하십시오. 
4. 서비스를 선택하거나 **모든 ID 및 액세스 사용 서비스**를 선택하십시오. 
5. 프롬프트되는 경우 **모든 현재 지역** 또는 특정 지역을 선택하십시오.
 
6. **모든 현재 서비스 인스턴스**를 선택하거나 특정 서비스 인스턴스를 선택하십시오. 
7. 선택한 서비스에 따라 다음 필드를 볼 수 있습니다. 이러한 필드에 값을 입력하지 않으면 버킷 레벨 대신 서비스 인스턴스 레벨에서 정책이 지정됩니다. 
    * **리소스 유형**: **버킷**을 입력하십시오.
    * **리소스 ID**: 버킷의 이름을 입력하십시오. 
8. 사용자에 대해 원하는 액세스를 지정하기 위한 역할의 임의의 조합을 선택하십시오. 
9. **지정**을 클릭하십시오.

사용자 액세스 관리, 리소스 그룹 작성 및 기타 모든 IAM 관리 태스크 완료 기능과 함께 모든 계정 리소스에 대한 사용자 액세스를 사용하려면 **관리자** 역할이 지정된 이 정책에 대해 **모든 ID 및 액세스 사용 서비스** 옵션을 선택하십시오.
{: tip}


## 액세스 제거

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스**를 클릭한 후에 **사용자**를 선택하십시오. 
2. 해당 액세스를 제거할 사용자 이름을 선택하십시오. 
3. 제거할 정책에 대한 행에서 **조치** 메뉴를 선택한 후에 **제거**를 클릭하십시오. 
4. 제거할 사용자 정책 세부사항을 검토한 후에 **제거**를 클릭하여 확인하십시오. 

## 지정된 액세스 검토

추가된 계정에서 지정된 액세스 권한을 검토해야 하는 경우에는 다음 단계를 완료하십시오. 

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스**를 클릭한 후에 **사용자**를 선택하십시오. 
2. 이름을 선택하십시오.
3. **액세스 정책** 섹션에서 지정된 액세스를 검토하십시오. 

추가 액세스가 필요한 경우에는 계정 소유자에게 문의하여 액세스를 업데이트하거나 서비스 또는 서비스 인스턴스의 관리자에게 문의하여 Cloud IAM 액세스 정책을 업데이트해야 합니다. 