---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 375eca319a1db467e97addac50faa3f91fe0ecc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920048"
---
# <span data-ttu-id="59dc8-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="59dc8-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="59dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="59dc8-103">Erhalten Sie eine oder mehrere Blaupausenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="59dc8-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="59dc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59dc8-104">SYNTAX</span></span>

### <span data-ttu-id="59dc8-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="59dc8-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59dc8-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="59dc8-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59dc8-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="59dc8-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59dc8-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="59dc8-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59dc8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59dc8-109">DESCRIPTION</span></span>
<span data-ttu-id="59dc8-110">Erhalten Sie eine oder mehrere Blaupausenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="59dc8-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="59dc8-111">Im Abonnementbereich sind Blaupausenzuordnungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="59dc8-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="59dc8-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59dc8-112">EXAMPLES</span></span>

### <span data-ttu-id="59dc8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59dc8-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="59dc8-114">Holen Sie sich die Blaupausenzuordnungen innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="59dc8-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="59dc8-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="59dc8-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="59dc8-116">Holen Sie sich die Blaupausenzuordnung mit dem angegebenen Namen innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="59dc8-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="59dc8-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="59dc8-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="59dc8-118">Holen Sie sich die Blaupausenzuordnungen innerhalb der angegebenen Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="59dc8-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="59dc8-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="59dc8-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="59dc8-120">Holen Sie sich die Blaupausenzuordnung mit dem angegebenen Namen innerhalb der angegebenen Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="59dc8-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="59dc8-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59dc8-121">PARAMETERS</span></span>

### <span data-ttu-id="59dc8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59dc8-122">-DefaultProfile</span></span>
<span data-ttu-id="59dc8-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59dc8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59dc8-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="59dc8-124">-ManagementGroupId</span></span>
<span data-ttu-id="59dc8-125">Die ID der Verwaltungsgruppe, in der die Blaupausenzuordnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="59dc8-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59dc8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="59dc8-126">-Name</span></span>
<span data-ttu-id="59dc8-127">Name der Blaupausenzuordnung.</span><span class="sxs-lookup"><span data-stu-id="59dc8-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59dc8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59dc8-128">-SubscriptionId</span></span>
<span data-ttu-id="59dc8-129">Abonnement-ID, für die die Blaupausenzuordnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="59dc8-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59dc8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59dc8-130">CommonParameters</span></span>
<span data-ttu-id="59dc8-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59dc8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59dc8-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59dc8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59dc8-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59dc8-133">INPUTS</span></span>

### <span data-ttu-id="59dc8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="59dc8-134">System.String</span></span>

## <span data-ttu-id="59dc8-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59dc8-135">OUTPUTS</span></span>

### <span data-ttu-id="59dc8-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="59dc8-136">System.Object</span></span>
## <span data-ttu-id="59dc8-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="59dc8-137">NOTES</span></span>

## <span data-ttu-id="59dc8-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="59dc8-138">RELATED LINKS</span></span>
