---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173185"
---
# <span data-ttu-id="57883-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="57883-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="57883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57883-102">SYNOPSIS</span></span>
<span data-ttu-id="57883-103">Nachverfolgen von Wartungsupdates für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57883-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="57883-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57883-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57883-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57883-105">DESCRIPTION</span></span>
<span data-ttu-id="57883-106">Nachverfolgen von Wartungsupdates für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57883-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="57883-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57883-107">EXAMPLES</span></span>

### <span data-ttu-id="57883-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57883-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="57883-109">Nachverfolgen von Wartungsupdates für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57883-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="57883-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57883-110">PARAMETERS</span></span>

### <span data-ttu-id="57883-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="57883-111">-ApplyUpdateName</span></span>
<span data-ttu-id="57883-112">Der Name der angewendeten Aktualisierungsressource.</span><span class="sxs-lookup"><span data-stu-id="57883-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57883-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57883-113">-DefaultProfile</span></span>
<span data-ttu-id="57883-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57883-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57883-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="57883-115">-ProviderName</span></span>
<span data-ttu-id="57883-116">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="57883-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57883-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57883-117">-ResourceGroupName</span></span>
<span data-ttu-id="57883-118">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="57883-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57883-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="57883-119">-ResourceName</span></span>
<span data-ttu-id="57883-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="57883-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57883-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="57883-121">-ResourceParentName</span></span>
<span data-ttu-id="57883-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="57883-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57883-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="57883-123">-ResourceParentType</span></span>
<span data-ttu-id="57883-124">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="57883-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57883-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="57883-125">-ResourceType</span></span>
<span data-ttu-id="57883-126">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="57883-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57883-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57883-127">CommonParameters</span></span>
<span data-ttu-id="57883-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57883-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57883-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57883-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57883-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57883-130">INPUTS</span></span>

### <span data-ttu-id="57883-131">System.String</span><span class="sxs-lookup"><span data-stu-id="57883-131">System.String</span></span>

## <span data-ttu-id="57883-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57883-132">OUTPUTS</span></span>

### <span data-ttu-id="57883-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="57883-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="57883-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="57883-134">NOTES</span></span>

## <span data-ttu-id="57883-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="57883-135">RELATED LINKS</span></span>
