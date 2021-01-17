---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459464"
---
# <span data-ttu-id="6fcb0-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="6fcb0-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="6fcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="6fcb0-103">Ruft Definitionen verwalteter Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="6fcb0-103">Gets managed application definitions</span></span>

## <span data-ttu-id="6fcb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fcb0-104">SYNTAX</span></span>

### <span data-ttu-id="6fcb0-105">GetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="6fcb0-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fcb0-106">GetById</span><span class="sxs-lookup"><span data-stu-id="6fcb0-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fcb0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fcb0-107">DESCRIPTION</span></span>
<span data-ttu-id="6fcb0-108">Das **Cmdlet "Get-AzManagedApplicationDefinition"** ruft verwaltete Anwendungsdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="6fcb0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fcb0-109">EXAMPLES</span></span>

### <span data-ttu-id="6fcb0-110">Beispiel 1: Alle Definitionen verwalteter Anwendungen unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="6fcb0-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="6fcb0-111">Mit diesem Befehl werden die Definitionen verwalteter Anwendungen unter der Ressourcengruppe "MyRG"</span><span class="sxs-lookup"><span data-stu-id="6fcb0-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="6fcb0-112">Beispiel 2: Erstellen einer Definition für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6fcb0-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="6fcb0-113">Dieser Befehl ruft die Definition der verwalteten Anwendung "myManagedAppDef" unter der Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="6fcb0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fcb0-114">PARAMETERS</span></span>

### <span data-ttu-id="6fcb0-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6fcb0-115">-ApiVersion</span></span>
<span data-ttu-id="6fcb0-116">Wenn dies festgelegt ist, wird die Version der zu verwendenden Ressourcenanbieter-API angegeben.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6fcb0-117">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fcb0-118">-DefaultProfile</span></span>
<span data-ttu-id="6fcb0-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fcb0-120">-ID</span><span class="sxs-lookup"><span data-stu-id="6fcb0-120">-Id</span></span>
<span data-ttu-id="6fcb0-121">Die vollqualifizierte Definitions-ID der verwalteten Anwendung, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="6fcb0-122">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6fcb0-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fcb0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6fcb0-123">-Name</span></span>
<span data-ttu-id="6fcb0-124">Der Name der verwalteten Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fcb0-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="6fcb0-125">-Pre</span></span>
<span data-ttu-id="6fcb0-126">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcb0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fcb0-127">-ResourceGroupName</span></span>
<span data-ttu-id="6fcb0-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fcb0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fcb0-129">CommonParameters</span></span>
<span data-ttu-id="6fcb0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fcb0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fcb0-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fcb0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fcb0-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fcb0-132">INPUTS</span></span>

### <span data-ttu-id="6fcb0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6fcb0-133">System.String</span></span>

## <span data-ttu-id="6fcb0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fcb0-134">OUTPUTS</span></span>

### <span data-ttu-id="6fcb0-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6fcb0-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6fcb0-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6fcb0-136">NOTES</span></span>

## <span data-ttu-id="6fcb0-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6fcb0-137">RELATED LINKS</span></span>
