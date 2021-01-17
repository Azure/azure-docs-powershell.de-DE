---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385858"
---
# <span data-ttu-id="7c2ce-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ce-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="7c2ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2ce-103">Listen Sie "configurationAssignments" für Die Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="7c2ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c2ce-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c2ce-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="7c2ce-106">Listen Sie "configurationAssignments" für Die Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="7c2ce-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c2ce-107">EXAMPLES</span></span>

### <span data-ttu-id="7c2ce-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c2ce-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="7c2ce-109">Listen Sie "configurationAssignments" für dedizierten Host auf.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="7c2ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c2ce-110">PARAMETERS</span></span>

### <span data-ttu-id="7c2ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2ce-111">-DefaultProfile</span></span>
<span data-ttu-id="7c2ce-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c2ce-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="7c2ce-113">-ProviderName</span></span>
<span data-ttu-id="7c2ce-114">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="7c2ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="7c2ce-116">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="7c2ce-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7c2ce-117">-ResourceName</span></span>
<span data-ttu-id="7c2ce-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-118">The resource name.</span></span>

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

### <span data-ttu-id="7c2ce-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="7c2ce-119">-ResourceParentName</span></span>
<span data-ttu-id="7c2ce-120">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-120">The parent resource name.</span></span>

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

### <span data-ttu-id="7c2ce-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="7c2ce-121">-ResourceParentType</span></span>
<span data-ttu-id="7c2ce-122">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-122">The parent resource type.</span></span>

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

### <span data-ttu-id="7c2ce-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7c2ce-123">-ResourceType</span></span>
<span data-ttu-id="7c2ce-124">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-124">The resource type.</span></span>

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

### <span data-ttu-id="7c2ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2ce-125">CommonParameters</span></span>
<span data-ttu-id="7c2ce-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2ce-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c2ce-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2ce-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c2ce-128">INPUTS</span></span>

### <span data-ttu-id="7c2ce-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7c2ce-129">System.String</span></span>

## <span data-ttu-id="7c2ce-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c2ce-130">OUTPUTS</span></span>

### <span data-ttu-id="7c2ce-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="7c2ce-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="7c2ce-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c2ce-132">NOTES</span></span>

## <span data-ttu-id="7c2ce-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c2ce-133">RELATED LINKS</span></span>
