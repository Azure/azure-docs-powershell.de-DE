---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177563"
---
# <span data-ttu-id="e0c37-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e0c37-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="e0c37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0c37-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c37-103">Listen Sie configurationAssignments für Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="e0c37-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="e0c37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0c37-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0c37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0c37-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c37-106">Listen Sie configurationAssignments für Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="e0c37-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="e0c37-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0c37-107">EXAMPLES</span></span>

### <span data-ttu-id="e0c37-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0c37-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="e0c37-109">Listen Sie configurationAssignments für dedizierten Host auf.</span><span class="sxs-lookup"><span data-stu-id="e0c37-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="e0c37-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0c37-110">PARAMETERS</span></span>

### <span data-ttu-id="e0c37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c37-111">-DefaultProfile</span></span>
<span data-ttu-id="e0c37-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0c37-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c37-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e0c37-113">-ProviderName</span></span>
<span data-ttu-id="e0c37-114">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="e0c37-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="e0c37-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0c37-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0c37-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0c37-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="e0c37-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e0c37-117">-ResourceName</span></span>
<span data-ttu-id="e0c37-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e0c37-118">The resource name.</span></span>

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

### <span data-ttu-id="e0c37-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e0c37-119">-ResourceParentName</span></span>
<span data-ttu-id="e0c37-120">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="e0c37-120">The parent resource name.</span></span>

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

### <span data-ttu-id="e0c37-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e0c37-121">-ResourceParentType</span></span>
<span data-ttu-id="e0c37-122">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="e0c37-122">The parent resource type.</span></span>

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

### <span data-ttu-id="e0c37-123">-</span><span class="sxs-lookup"><span data-stu-id="e0c37-123">-ResourceType</span></span>
<span data-ttu-id="e0c37-124">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="e0c37-124">The resource type.</span></span>

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

### <span data-ttu-id="e0c37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c37-125">CommonParameters</span></span>
<span data-ttu-id="e0c37-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c37-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0c37-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c37-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0c37-128">INPUTS</span></span>

### <span data-ttu-id="e0c37-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e0c37-129">System.String</span></span>

## <span data-ttu-id="e0c37-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0c37-130">OUTPUTS</span></span>

### <span data-ttu-id="e0c37-131">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e0c37-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="e0c37-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0c37-132">NOTES</span></span>

## <span data-ttu-id="e0c37-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0c37-133">RELATED LINKS</span></span>
