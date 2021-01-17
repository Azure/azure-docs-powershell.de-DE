---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471043"
---
# <span data-ttu-id="189af-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="189af-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="189af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="189af-102">SYNOPSIS</span></span>
<span data-ttu-id="189af-103">Erhalten Sie eine oder mehrere Blaupausenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="189af-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="189af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="189af-104">SYNTAX</span></span>

### <span data-ttu-id="189af-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="189af-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="189af-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="189af-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="189af-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="189af-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="189af-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="189af-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="189af-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="189af-109">DESCRIPTION</span></span>
<span data-ttu-id="189af-110">Erhalten Sie eine oder mehrere Blaupausenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="189af-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="189af-111">Blaupausenzuweisungen sind im Abonnementbereich vorhanden.</span><span class="sxs-lookup"><span data-stu-id="189af-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="189af-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="189af-112">EXAMPLES</span></span>

### <span data-ttu-id="189af-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="189af-113">Example 1</span></span>
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

<span data-ttu-id="189af-114">Holen Sie sich die Blaupausenaufgaben innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="189af-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="189af-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="189af-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="189af-116">Erhalten Sie die Blaupausenaufgabe mit dem angegebenen Namen innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="189af-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="189af-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="189af-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="189af-118">Erhalten Sie die Blaupausenaufgaben in der angegebenen Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="189af-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="189af-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="189af-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="189af-120">Erhalten Sie die Blaupausenaufgabe mit dem angegebenen Namen in der angegebenen Managementgruppe.</span><span class="sxs-lookup"><span data-stu-id="189af-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="189af-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="189af-121">PARAMETERS</span></span>

### <span data-ttu-id="189af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189af-122">-DefaultProfile</span></span>
<span data-ttu-id="189af-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="189af-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="189af-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="189af-124">-ManagementGroupId</span></span>
<span data-ttu-id="189af-125">Die ID der Verwaltungsgruppe, in der die Blaupausenzuweisung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="189af-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="189af-126">-Name</span><span class="sxs-lookup"><span data-stu-id="189af-126">-Name</span></span>
<span data-ttu-id="189af-127">Name der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="189af-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="189af-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="189af-128">-SubscriptionId</span></span>
<span data-ttu-id="189af-129">Abonnement-ID, für die die Blaupausenzuweisung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="189af-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="189af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189af-130">CommonParameters</span></span>
<span data-ttu-id="189af-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="189af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189af-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="189af-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189af-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="189af-133">INPUTS</span></span>

### <span data-ttu-id="189af-134">System.String</span><span class="sxs-lookup"><span data-stu-id="189af-134">System.String</span></span>

## <span data-ttu-id="189af-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="189af-135">OUTPUTS</span></span>

### <span data-ttu-id="189af-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="189af-136">System.Object</span></span>
## <span data-ttu-id="189af-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="189af-137">NOTES</span></span>

## <span data-ttu-id="189af-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="189af-138">RELATED LINKS</span></span>
