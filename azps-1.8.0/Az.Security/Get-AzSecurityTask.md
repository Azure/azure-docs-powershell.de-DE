---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
ms.openlocfilehash: 9d1ce9dc517e550fdfada1db000657aedc15c6ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659446"
---
# <span data-ttu-id="35cc0-101">Get-AzSecurityTask</span><span class="sxs-lookup"><span data-stu-id="35cc0-101">Get-AzSecurityTask</span></span>

## <span data-ttu-id="35cc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="35cc0-103">Ruft die Sicherheitsaufgaben ab, die von Azure Security Center empfohlen werden, um Ihre Sicherheitsposition zu stärken.</span><span class="sxs-lookup"><span data-stu-id="35cc0-103">Gets the security tasks that Azure Security Center recommends you to do in order to strengthen your security posture.</span></span>

## <span data-ttu-id="35cc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35cc0-104">SYNTAX</span></span>

### <span data-ttu-id="35cc0-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="35cc0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35cc0-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="35cc0-106">ResourceGroupScope</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35cc0-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="35cc0-107">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35cc0-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="35cc0-108">SubscriptionLevelResource</span></span>
```
Get-AzSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35cc0-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="35cc0-109">ResourceId</span></span>
```
Get-AzSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35cc0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35cc0-110">DESCRIPTION</span></span>
<span data-ttu-id="35cc0-111">Azure Security Center scannt Ihre Ressourcen, um potenzielle Sicherheitsprobleme zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="35cc0-111">Azure Security Center scans your resources to detect potential security issues.</span></span>
<span data-ttu-id="35cc0-112">Mit diesem Cmdlet können Sie die Sicherheitsaufgaben ermitteln, die von Azure Security Center empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="35cc0-112">This cmdlet lets you discover the security tasks that Azure Security Center recommends you to do.</span></span>

## <span data-ttu-id="35cc0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35cc0-113">EXAMPLES</span></span>

### <span data-ttu-id="35cc0-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35cc0-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

<span data-ttu-id="35cc0-115">Ruft alle Sicherheitsaufgaben ab, die für Ressourcen innerhalb eines Abonnements ermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="35cc0-115">Gets all the security tasks that were discovered on resources inside a subscription.</span></span>

### <span data-ttu-id="35cc0-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35cc0-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1"

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

<span data-ttu-id="35cc0-117">Ruft alle Sicherheitsaufgaben ab, die für Ressourcen innerhalb einer Ressourcengruppe ermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="35cc0-117">Gets all the security tasks that were discovered on resources inside a resource group.</span></span>

### <span data-ttu-id="35cc0-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="35cc0-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

<span data-ttu-id="35cc0-119">Ruft eine bestimmte Sicherheitsaufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="35cc0-119">Gets a specific security task.</span></span>

## <span data-ttu-id="35cc0-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="35cc0-120">PARAMETERS</span></span>

### <span data-ttu-id="35cc0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cc0-121">-DefaultProfile</span></span>
<span data-ttu-id="35cc0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35cc0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35cc0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="35cc0-123">-Name</span></span>
<span data-ttu-id="35cc0-124">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="35cc0-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35cc0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35cc0-125">-ResourceGroupName</span></span>
<span data-ttu-id="35cc0-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35cc0-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35cc0-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="35cc0-127">-ResourceId</span></span>
<span data-ttu-id="35cc0-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="35cc0-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35cc0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cc0-129">CommonParameters</span></span>
<span data-ttu-id="35cc0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35cc0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cc0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35cc0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cc0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35cc0-132">INPUTS</span></span>

### <span data-ttu-id="35cc0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="35cc0-133">System.String</span></span>

## <span data-ttu-id="35cc0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35cc0-134">OUTPUTS</span></span>

### <span data-ttu-id="35cc0-135">Microsoft. Azure. Commands. Security. Models. Tasks. PSSecurityTask</span><span class="sxs-lookup"><span data-stu-id="35cc0-135">Microsoft.Azure.Commands.Security.Models.Tasks.PSSecurityTask</span></span>

## <span data-ttu-id="35cc0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="35cc0-136">NOTES</span></span>

## <span data-ttu-id="35cc0-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35cc0-137">RELATED LINKS</span></span>
