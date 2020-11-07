---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: af03fa8e29ab5912fb3e2d1809c9e2fc67941fb5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846328"
---
# <span data-ttu-id="324e2-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="324e2-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="324e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="324e2-102">SYNOPSIS</span></span>
<span data-ttu-id="324e2-103">Abrufen von Problem Klassifikationen für den angegebenen Dienst</span><span class="sxs-lookup"><span data-stu-id="324e2-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="324e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="324e2-104">SYNTAX</span></span>

### <span data-ttu-id="324e2-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="324e2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="324e2-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="324e2-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="324e2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="324e2-107">DESCRIPTION</span></span>
<span data-ttu-id="324e2-108">Ruft die aktuelle Liste der Problemklassifizierung für einen Azure-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="324e2-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="324e2-109">Sie können die GUID des Diensts und der Problemklassifizierung verwenden, um ein neues Support Ticket mithilfe von New-AzSupportTicket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="324e2-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="324e2-110">Verwenden Sie immer die GUIDs des Diensts und der Problemklassifizierung, die programmgesteuert abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="324e2-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="324e2-111">Diese Vorgehensweise stellt sicher, dass Sie über die neuesten GUIDs für Dienst-und Problem Klassifikationen für die Erstellung von Support Tickets verfügen.</span><span class="sxs-lookup"><span data-stu-id="324e2-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="324e2-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="324e2-112">EXAMPLES</span></span>

### <span data-ttu-id="324e2-113">Beispiel 1: Abrufen aller Problem classificaitons für einen Dienst mithilfe des Dienst-ID-Parameters.</span><span class="sxs-lookup"><span data-stu-id="324e2-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
```powershell
PS C:\> Get-AzSupportProblemClassification -ServiceId "{vm_running_windows_service_guid}"

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="324e2-114">Beispiel 2: Abrufen aller Problem classificaitons für einen Dienst mit dem übergeordneten Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="324e2-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification 

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="324e2-115">Beispiel 3: Abrufen von Details zu einem einzelnen Problem classificaiton nach ID nach dem Rohrleitungs Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="324e2-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="324e2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="324e2-116">PARAMETERS</span></span>

### <span data-ttu-id="324e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324e2-117">-DefaultProfile</span></span>
<span data-ttu-id="324e2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="324e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324e2-119">-ID</span><span class="sxs-lookup"><span data-stu-id="324e2-119">-Id</span></span>
<span data-ttu-id="324e2-120">Problem Klassifikations-ID.</span><span class="sxs-lookup"><span data-stu-id="324e2-120">Problem classification id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324e2-121">-Service-Nr</span><span class="sxs-lookup"><span data-stu-id="324e2-121">-ServiceId</span></span>
<span data-ttu-id="324e2-122">Dienst-ID, für die alle Problem Klassifikationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="324e2-122">Service id for which all problem classifications are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324e2-123">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="324e2-123">-ServiceObject</span></span>
<span data-ttu-id="324e2-124">Dienstobjekt, für das Problem Klassifikationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="324e2-124">Service object for which problem classifications are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportService
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="324e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324e2-125">CommonParameters</span></span>
<span data-ttu-id="324e2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="324e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324e2-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="324e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324e2-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="324e2-128">INPUTS</span></span>

### <span data-ttu-id="324e2-129">Microsoft. Azure. Commands. Support. Models. PSSupportService</span><span class="sxs-lookup"><span data-stu-id="324e2-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="324e2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="324e2-130">OUTPUTS</span></span>

### <span data-ttu-id="324e2-131">Microsoft. Azure. Commands. Support. Models. PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="324e2-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="324e2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="324e2-132">NOTES</span></span>

## <span data-ttu-id="324e2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="324e2-133">RELATED LINKS</span></span>
