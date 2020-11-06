---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501413"
---
# <span data-ttu-id="c404c-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c404c-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="c404c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c404c-102">SYNOPSIS</span></span>
<span data-ttu-id="c404c-103">Ruft Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="c404c-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c404c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c404c-104">SYNTAX</span></span>

### <span data-ttu-id="c404c-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="c404c-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c404c-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c404c-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c404c-107">GetById</span><span class="sxs-lookup"><span data-stu-id="c404c-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c404c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c404c-108">DESCRIPTION</span></span>
<span data-ttu-id="c404c-109">Das Cmdlet " **Get-AzureRmPolicySetDefinition** " ruft alle Richtliniensatz Definitionen oder eine bestimmte Richtliniensatz Definition ab, die durch den Namen oder die ID identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="c404c-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="c404c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c404c-110">EXAMPLES</span></span>

### <span data-ttu-id="c404c-111">Beispiel 1: Abrufen der gesamten Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="c404c-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="c404c-112">Dieser Befehl ruft alle Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="c404c-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="c404c-113">Beispiel 2: Abrufen der Richtliniensatz Definition nach Name</span><span class="sxs-lookup"><span data-stu-id="c404c-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="c404c-114">Dieser Befehl ruft die Richtliniensatz Definition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="c404c-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="c404c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c404c-115">PARAMETERS</span></span>

### <span data-ttu-id="c404c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c404c-116">-ApiVersion</span></span>
<span data-ttu-id="c404c-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c404c-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c404c-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c404c-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c404c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c404c-119">-DefaultProfile</span></span>
<span data-ttu-id="c404c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c404c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c404c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c404c-121">-Id</span></span>
<span data-ttu-id="c404c-122">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c404c-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="c404c-123">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c404c-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c404c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c404c-124">-Name</span></span>
<span data-ttu-id="c404c-125">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="c404c-125">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c404c-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="c404c-126">-Pre</span></span>
<span data-ttu-id="c404c-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c404c-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c404c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c404c-128">CommonParameters</span></span>
<span data-ttu-id="c404c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c404c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c404c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c404c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c404c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c404c-131">INPUTS</span></span>

### <span data-ttu-id="c404c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c404c-132">System.String</span></span>

## <span data-ttu-id="c404c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c404c-133">OUTPUTS</span></span>

### <span data-ttu-id="c404c-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c404c-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c404c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c404c-135">NOTES</span></span>

## <span data-ttu-id="c404c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c404c-136">RELATED LINKS</span></span>
