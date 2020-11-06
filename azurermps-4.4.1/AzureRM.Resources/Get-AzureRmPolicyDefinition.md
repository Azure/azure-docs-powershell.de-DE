---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503214"
---
# <span data-ttu-id="0d482-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d482-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="0d482-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d482-102">SYNOPSIS</span></span>
<span data-ttu-id="0d482-103">Ruft Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="0d482-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d482-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d482-104">SYNTAX</span></span>

### <span data-ttu-id="0d482-105">Der Parametersatz Liste alle Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="0d482-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="0d482-106">Standard</span><span class="sxs-lookup"><span data-stu-id="0d482-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d482-107">Der Parametersatz für den Richtlinien Definitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="0d482-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d482-108">Der Parametersatz für die Richtlinien Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="0d482-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0d482-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d482-109">DESCRIPTION</span></span>
<span data-ttu-id="0d482-110">Das Cmdlet " **Get-AzureRmPolicyDefinition** " ruft alle Richtlinien Definitionen oder eine bestimmte Richtliniendefinition ab, die durch den Namen oder die ID identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0d482-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="0d482-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d482-111">EXAMPLES</span></span>

### <span data-ttu-id="0d482-112">Beispiel 1: Abrufen der gesamten Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="0d482-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="0d482-113">Dieser Befehl ruft alle Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="0d482-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="0d482-114">Beispiel 2: Abrufen der Richtliniendefinition nach Name</span><span class="sxs-lookup"><span data-stu-id="0d482-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="0d482-115">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="0d482-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="0d482-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d482-116">PARAMETERS</span></span>

### <span data-ttu-id="0d482-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d482-117">-ApiVersion</span></span>
<span data-ttu-id="0d482-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="0d482-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0d482-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="0d482-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0d482-120">-ID</span><span class="sxs-lookup"><span data-stu-id="0d482-120">-Id</span></span>
<span data-ttu-id="0d482-121">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0d482-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d482-122">-Information</span><span class="sxs-lookup"><span data-stu-id="0d482-122">-InformationAction</span></span>
<span data-ttu-id="0d482-123">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="0d482-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0d482-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0d482-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d482-125">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="0d482-125">Continue</span></span>
- <span data-ttu-id="0d482-126">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0d482-126">Ignore</span></span>
- <span data-ttu-id="0d482-127">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="0d482-127">Inquire</span></span>
- <span data-ttu-id="0d482-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0d482-128">SilentlyContinue</span></span>
- <span data-ttu-id="0d482-129">Beenden</span><span class="sxs-lookup"><span data-stu-id="0d482-129">Stop</span></span>
- <span data-ttu-id="0d482-130">Anhalten</span><span class="sxs-lookup"><span data-stu-id="0d482-130">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d482-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0d482-131">-InformationVariable</span></span>
<span data-ttu-id="0d482-132">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="0d482-132">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d482-133">-Name</span><span class="sxs-lookup"><span data-stu-id="0d482-133">-Name</span></span>
<span data-ttu-id="0d482-134">Gibt den Namen der Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0d482-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d482-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d482-135">-Pre</span></span>
<span data-ttu-id="0d482-136">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0d482-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0d482-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d482-137">-DefaultProfile</span></span>
<span data-ttu-id="0d482-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d482-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d482-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d482-139">CommonParameters</span></span>
<span data-ttu-id="0d482-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d482-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d482-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d482-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d482-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d482-142">INPUTS</span></span>

## <span data-ttu-id="0d482-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d482-143">OUTPUTS</span></span>

### <span data-ttu-id="0d482-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0d482-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0d482-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d482-145">NOTES</span></span>

## <span data-ttu-id="0d482-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d482-146">RELATED LINKS</span></span>

[<span data-ttu-id="0d482-147">Neu – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d482-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="0d482-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d482-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="0d482-149">Satz-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d482-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


