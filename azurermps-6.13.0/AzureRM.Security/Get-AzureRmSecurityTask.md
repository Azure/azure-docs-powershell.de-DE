---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
ms.openlocfilehash: 51c2772a891cf39ba780c6ff3da0af40170f477e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477690"
---
# <span data-ttu-id="16042-101">Get-AzureRmSecurityTask</span><span class="sxs-lookup"><span data-stu-id="16042-101">Get-AzureRmSecurityTask</span></span>

## <span data-ttu-id="16042-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16042-102">SYNOPSIS</span></span>
<span data-ttu-id="16042-103">Ruft die Sicherheitsaufgaben ab, die von Azure Security Center empfohlen werden, um Ihre Sicherheitsposition zu stärken.</span><span class="sxs-lookup"><span data-stu-id="16042-103">Gets the security tasks that Azure Security Center recommends you to do in order to strengthen your security posture.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16042-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16042-104">SYNTAX</span></span>

### <span data-ttu-id="16042-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="16042-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16042-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="16042-106">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16042-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="16042-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16042-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="16042-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16042-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="16042-109">ResourceId</span></span>
```
Get-AzureRmSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16042-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16042-110">DESCRIPTION</span></span>
<span data-ttu-id="16042-111">Azure Security Center scannt Ihre Ressourcen, um potenzielle Sicherheitsprobleme zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="16042-111">Azure Security Center scans your resources to detect potential security issues.</span></span>
<span data-ttu-id="16042-112">Mit diesem Cmdlet können Sie die Sicherheitsaufgaben ermitteln, die von Azure Security Center empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="16042-112">This cmdlet lets you discover the security tasks that Azure Security Center recommends you to do.</span></span>

## <span data-ttu-id="16042-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16042-113">EXAMPLES</span></span>

### <span data-ttu-id="16042-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16042-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

<span data-ttu-id="16042-115">Ruft alle Sicherheitsaufgaben ab, die für Ressourcen innerhalb eines Abonnements ermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="16042-115">Gets all the security tasks that were discovered on resources inside a subscription.</span></span>

### <span data-ttu-id="16042-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="16042-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask -ResourceGroupName "myService1"

Id                                                                                                                                                                        Name                                 RecommendationType                   ResourceI
                                                                                                                                                                                                                                                    d        
--                                                                                                                                                                        ----                                 ------------------                   ---------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/47f736fa-0ec8-a372-de49-8cf18527930c 47f736fa-0ec8-a372-de49-8cf18527930c ConfigureTier2Waf                    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/5696e90f-833d-494c-8833-f3be335fa9cb 5696e90f-833d-494c-8833-f3be335fa9cb NetworkSecurityGroupMissingOnVm      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/65193cce-25a1-b30f-f94e-69d52e22923c 65193cce-25a1-b30f-f94e-69d52e22923c VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/7e28a40d-e746-4751-8340-5126d6b77ae5 7e28a40d-e746-4751-8340-5126d6b77ae5 NetworkSecurityGroupMissingOnSubnet  /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/94867597-75e5-cfb6-8b71-e5e5253a24e1 94867597-75e5-cfb6-8b71-e5e5253a24e1 EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/a02fffd5-1956-a6d7-73da-a87a65ae02f4 a02fffd5-1956-a6d7-73da-a87a65ae02f4 VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/bd382d04-b478-ac77-e89f-300789032367 bd382d04-b478-ac77-e89f-300789032367 ProvisionNgfw                        /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/ce43626a-d56b-6a38-49ef-3ad7a731666e ce43626a-d56b-6a38-49ef-3ad7a731666e EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/dcfb6365-799e-5ed4-f344-d86a0a4c2992 dcfb6365-799e-5ed4-f344-d86a0a4c2992 Enable auditing for the SQL database /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/ed736ed1-3f42-a95a-0b9e-458c44233937 ed736ed1-3f42-a95a-0b9e-458c44233937 Enable auditing for the SQL server   /subsc...
```

<span data-ttu-id="16042-117">Ruft alle Sicherheitsaufgaben ab, die für Ressourcen innerhalb einer Ressourcengruppe ermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="16042-117">Gets all the security tasks that were discovered on resources inside a resource group.</span></span>

### <span data-ttu-id="16042-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="16042-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

<span data-ttu-id="16042-119">Ruft eine bestimmte Sicherheitsaufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="16042-119">Gets a specific security task.</span></span>

## <span data-ttu-id="16042-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="16042-120">PARAMETERS</span></span>

### <span data-ttu-id="16042-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16042-121">-DefaultProfile</span></span>
<span data-ttu-id="16042-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16042-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16042-123">-Name</span><span class="sxs-lookup"><span data-stu-id="16042-123">-Name</span></span>
<span data-ttu-id="16042-124">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="16042-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16042-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16042-125">-ResourceGroupName</span></span>
<span data-ttu-id="16042-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="16042-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16042-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16042-127">-ResourceId</span></span>
<span data-ttu-id="16042-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="16042-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16042-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16042-129">CommonParameters</span></span>
<span data-ttu-id="16042-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16042-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16042-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16042-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16042-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16042-132">INPUTS</span></span>

### <span data-ttu-id="16042-133">System. String</span><span class="sxs-lookup"><span data-stu-id="16042-133">System.String</span></span>

## <span data-ttu-id="16042-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16042-134">OUTPUTS</span></span>

### <span data-ttu-id="16042-135">Microsoft. Azure. Commands. Security. Models. Tasks. PSSecurityTask</span><span class="sxs-lookup"><span data-stu-id="16042-135">Microsoft.Azure.Commands.Security.Models.Tasks.PSSecurityTask</span></span>

## <span data-ttu-id="16042-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="16042-136">NOTES</span></span>

## <span data-ttu-id="16042-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16042-137">RELATED LINKS</span></span>
