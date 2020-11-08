---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008679"
---
# <span data-ttu-id="d9667-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d9667-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="d9667-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9667-102">SYNOPSIS</span></span>
<span data-ttu-id="d9667-103">Besorgen Sie sich eine oder mehrere Blueprint-Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d9667-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="d9667-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9667-104">SYNTAX</span></span>

### <span data-ttu-id="d9667-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9667-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9667-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="d9667-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9667-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="d9667-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9667-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="d9667-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9667-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9667-109">DESCRIPTION</span></span>
<span data-ttu-id="d9667-110">Besorgen Sie sich eine oder mehrere Blueprint-Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d9667-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="d9667-111">Blueprint-Aufgaben sind im Abonnement Bereich vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9667-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="d9667-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9667-112">EXAMPLES</span></span>

### <span data-ttu-id="d9667-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9667-113">Example 1</span></span>
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

<span data-ttu-id="d9667-114">Abrufen der Blueprint-Aufgaben innerhalb des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="d9667-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="d9667-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d9667-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="d9667-116">Rufen Sie die Blueprint-Zuordnung mit dem angegebenen Namen innerhalb des angegebenen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="d9667-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="d9667-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d9667-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="d9667-118">Rufen Sie die Blueprint-Aufgaben in der angegebenen Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="d9667-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="d9667-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d9667-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="d9667-120">Rufen Sie die Blueprint-Zuordnung mit dem angegebenen Namen innerhalb der angegebenen Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="d9667-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="d9667-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9667-121">PARAMETERS</span></span>

### <span data-ttu-id="d9667-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9667-122">-DefaultProfile</span></span>
<span data-ttu-id="d9667-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9667-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9667-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d9667-124">-ManagementGroupId</span></span>
<span data-ttu-id="d9667-125">Die ID der Verwaltungsgruppe, in der die Blueprint-Zuordnung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d9667-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="d9667-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d9667-126">-Name</span></span>
<span data-ttu-id="d9667-127">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="d9667-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="d9667-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d9667-128">-SubscriptionId</span></span>
<span data-ttu-id="d9667-129">Die Abonnement-ID, in der die Blueprint-Aufgabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d9667-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="d9667-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9667-130">CommonParameters</span></span>
<span data-ttu-id="d9667-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9667-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9667-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9667-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9667-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9667-133">INPUTS</span></span>

### <span data-ttu-id="d9667-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d9667-134">System.String</span></span>

## <span data-ttu-id="d9667-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9667-135">OUTPUTS</span></span>

### <span data-ttu-id="d9667-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="d9667-136">System.Object</span></span>
## <span data-ttu-id="d9667-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9667-137">NOTES</span></span>

## <span data-ttu-id="d9667-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9667-138">RELATED LINKS</span></span>
