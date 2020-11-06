---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500773"
---
# <span data-ttu-id="87228-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="87228-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="87228-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87228-102">SYNOPSIS</span></span>
<span data-ttu-id="87228-103">Ruft Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="87228-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87228-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87228-104">SYNTAX</span></span>

### <span data-ttu-id="87228-105">Der Parametersatz Listen alle Richtliniensatz-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="87228-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="87228-106">Standard</span><span class="sxs-lookup"><span data-stu-id="87228-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87228-107">Der Parametersatz für den Richtliniensatz-Definitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="87228-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87228-108">Der Parametersatz für die Richtliniensatz-Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="87228-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87228-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87228-109">DESCRIPTION</span></span>
<span data-ttu-id="87228-110">Das Cmdlet " **Get-AzureRmPolicySetDefinition** " ruft alle Richtliniensatz Definitionen oder eine bestimmte Richtliniensatz Definition ab, die durch den Namen oder die ID identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="87228-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="87228-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87228-111">EXAMPLES</span></span>

### <span data-ttu-id="87228-112">Beispiel 1: Abrufen der gesamten Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="87228-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="87228-113">Dieser Befehl ruft alle Richtliniensatz Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="87228-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="87228-114">Beispiel 2: Abrufen der Richtliniensatz Definition nach Name</span><span class="sxs-lookup"><span data-stu-id="87228-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="87228-115">Dieser Befehl ruft die Richtliniensatz Definition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="87228-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="87228-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="87228-116">PARAMETERS</span></span>

### <span data-ttu-id="87228-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="87228-117">-ApiVersion</span></span>
<span data-ttu-id="87228-118">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87228-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="87228-119">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="87228-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="87228-120">-ID</span><span class="sxs-lookup"><span data-stu-id="87228-120">-Id</span></span>
<span data-ttu-id="87228-121">Die vollqualifizierte Richtliniensatz-Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="87228-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="87228-122">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="87228-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87228-123">-Name</span><span class="sxs-lookup"><span data-stu-id="87228-123">-Name</span></span>
<span data-ttu-id="87228-124">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="87228-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87228-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="87228-125">-Pre</span></span>
<span data-ttu-id="87228-126">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="87228-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="87228-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87228-127">-DefaultProfile</span></span>
<span data-ttu-id="87228-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87228-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87228-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87228-129">CommonParameters</span></span>
<span data-ttu-id="87228-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87228-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87228-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87228-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87228-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87228-132">INPUTS</span></span>

### <span data-ttu-id="87228-133">System. String</span><span class="sxs-lookup"><span data-stu-id="87228-133">System.String</span></span>

## <span data-ttu-id="87228-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87228-134">OUTPUTS</span></span>

### <span data-ttu-id="87228-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="87228-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="87228-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="87228-136">NOTES</span></span>

## <span data-ttu-id="87228-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87228-137">RELATED LINKS</span></span>

