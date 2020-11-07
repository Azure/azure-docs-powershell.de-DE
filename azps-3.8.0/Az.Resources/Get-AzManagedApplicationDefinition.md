---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846795"
---
# <span data-ttu-id="639af-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="639af-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="639af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="639af-102">SYNOPSIS</span></span>
<span data-ttu-id="639af-103">Ruft Definitionen für verwaltete Anwendungen ab</span><span class="sxs-lookup"><span data-stu-id="639af-103">Gets managed application definitions</span></span>

## <span data-ttu-id="639af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="639af-104">SYNTAX</span></span>

### <span data-ttu-id="639af-105">GetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="639af-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="639af-106">GetById</span><span class="sxs-lookup"><span data-stu-id="639af-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="639af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="639af-107">DESCRIPTION</span></span>
<span data-ttu-id="639af-108">Das Cmdlet " **Get-AzManagedApplicationDefinition** " ruft verwaltete Anwendungsdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="639af-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="639af-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="639af-109">EXAMPLES</span></span>

### <span data-ttu-id="639af-110">Beispiel 1: Abrufen aller verwalteten Anwendungsdefinitionen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="639af-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="639af-111">Dieser Befehl ruft die Definitionen verwalteter Anwendungen unter Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="639af-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="639af-112">Beispiel 2: Abrufen einer Definition einer verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="639af-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="639af-113">Dieser Befehl ruft die verwaltete Anwendungsdefinition "myManagedAppDef" unter Ressourcengruppe "MyRG" ab.</span><span class="sxs-lookup"><span data-stu-id="639af-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="639af-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="639af-114">PARAMETERS</span></span>

### <span data-ttu-id="639af-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="639af-115">-ApiVersion</span></span>
<span data-ttu-id="639af-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="639af-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="639af-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="639af-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="639af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639af-118">-DefaultProfile</span></span>
<span data-ttu-id="639af-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="639af-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="639af-120">-ID</span><span class="sxs-lookup"><span data-stu-id="639af-120">-Id</span></span>
<span data-ttu-id="639af-121">Die vollqualifizierte Definitions-ID der verwalteten Anwendung einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="639af-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="639af-122">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="639af-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="639af-123">-Name</span><span class="sxs-lookup"><span data-stu-id="639af-123">-Name</span></span>
<span data-ttu-id="639af-124">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="639af-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="639af-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="639af-125">-Pre</span></span>
<span data-ttu-id="639af-126">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="639af-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="639af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639af-127">-ResourceGroupName</span></span>
<span data-ttu-id="639af-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="639af-128">The resource group name.</span></span>

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

### <span data-ttu-id="639af-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639af-129">CommonParameters</span></span>
<span data-ttu-id="639af-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="639af-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639af-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="639af-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639af-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="639af-132">INPUTS</span></span>

### <span data-ttu-id="639af-133">System. String</span><span class="sxs-lookup"><span data-stu-id="639af-133">System.String</span></span>

## <span data-ttu-id="639af-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="639af-134">OUTPUTS</span></span>

### <span data-ttu-id="639af-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="639af-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="639af-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="639af-136">NOTES</span></span>

## <span data-ttu-id="639af-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="639af-137">RELATED LINKS</span></span>
