---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459468"
---
# <span data-ttu-id="eb331-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="eb331-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="eb331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb331-102">SYNOPSIS</span></span>
<span data-ttu-id="eb331-103">Bekommt verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="eb331-103">Gets managed applications</span></span>

## <span data-ttu-id="eb331-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb331-104">SYNTAX</span></span>

### <span data-ttu-id="eb331-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb331-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb331-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eb331-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb331-107">GetById</span><span class="sxs-lookup"><span data-stu-id="eb331-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb331-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb331-108">DESCRIPTION</span></span>
<span data-ttu-id="eb331-109">Das **Cmdlet "Get-AzManagedApplication"** ruft verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="eb331-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="eb331-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb331-110">EXAMPLES</span></span>

### <span data-ttu-id="eb331-111">Beispiel 1: Alle verwalteten Anwendungen unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="eb331-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="eb331-112">Dieser Befehl ruft verwaltete Anwendungen unter der Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="eb331-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="eb331-113">Beispiel 2: Alle verwalteten Anwendungen erhalten</span><span class="sxs-lookup"><span data-stu-id="eb331-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="eb331-114">Mit diesem Befehl werden alle verwalteten Anwendungen unter dem aktuellen Abonnement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eb331-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="eb331-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb331-115">PARAMETERS</span></span>

### <span data-ttu-id="eb331-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eb331-116">-ApiVersion</span></span>
<span data-ttu-id="eb331-117">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="eb331-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="eb331-118">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="eb331-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="eb331-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb331-119">-DefaultProfile</span></span>
<span data-ttu-id="eb331-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb331-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb331-121">-ID</span><span class="sxs-lookup"><span data-stu-id="eb331-121">-Id</span></span>
<span data-ttu-id="eb331-122">Die vollqualifizierte verwaltete Anwendungs-ID einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="eb331-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="eb331-123">z. B. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="eb331-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb331-124">-Name</span><span class="sxs-lookup"><span data-stu-id="eb331-124">-Name</span></span>
<span data-ttu-id="eb331-125">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="eb331-125">The managed application name.</span></span>

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

### <span data-ttu-id="eb331-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="eb331-126">-Pre</span></span>
<span data-ttu-id="eb331-127">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb331-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eb331-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb331-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb331-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb331-129">The resource group name.</span></span>

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

### <span data-ttu-id="eb331-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb331-130">CommonParameters</span></span>
<span data-ttu-id="eb331-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb331-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb331-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb331-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb331-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb331-133">INPUTS</span></span>

### <span data-ttu-id="eb331-134">System.String</span><span class="sxs-lookup"><span data-stu-id="eb331-134">System.String</span></span>

## <span data-ttu-id="eb331-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb331-135">OUTPUTS</span></span>

### <span data-ttu-id="eb331-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="eb331-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eb331-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb331-137">NOTES</span></span>

## <span data-ttu-id="eb331-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb331-138">RELATED LINKS</span></span>
