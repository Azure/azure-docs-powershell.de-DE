---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501422"
---
# <span data-ttu-id="4be27-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4be27-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="4be27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4be27-102">SYNOPSIS</span></span>
<span data-ttu-id="4be27-103">Ruft Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="4be27-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4be27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4be27-104">SYNTAX</span></span>

### <span data-ttu-id="4be27-105">GetAllPolicyDefinitions (Standard)</span><span class="sxs-lookup"><span data-stu-id="4be27-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4be27-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="4be27-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4be27-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4be27-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4be27-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4be27-108">DESCRIPTION</span></span>
<span data-ttu-id="4be27-109">Das Cmdlet " **Get-AzureRmPolicyDefinition** " ruft alle Richtlinien Definitionen oder eine bestimmte Richtliniendefinition ab, die durch den Namen oder die ID identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4be27-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="4be27-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4be27-110">EXAMPLES</span></span>

### <span data-ttu-id="4be27-111">Beispiel 1: Abrufen der gesamten Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="4be27-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="4be27-112">Dieser Befehl ruft alle Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="4be27-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="4be27-113">Beispiel 2: Abrufen der Richtliniendefinition nach Name</span><span class="sxs-lookup"><span data-stu-id="4be27-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="4be27-114">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="4be27-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="4be27-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4be27-115">PARAMETERS</span></span>

### <span data-ttu-id="4be27-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4be27-116">-ApiVersion</span></span>
<span data-ttu-id="4be27-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="4be27-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4be27-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="4be27-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4be27-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be27-119">-DefaultProfile</span></span>
<span data-ttu-id="4be27-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4be27-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4be27-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4be27-121">-Id</span></span>
<span data-ttu-id="4be27-122">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4be27-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be27-123">-Information</span><span class="sxs-lookup"><span data-stu-id="4be27-123">-InformationAction</span></span>
<span data-ttu-id="4be27-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4be27-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4be27-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4be27-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4be27-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4be27-126">Continue</span></span>
- <span data-ttu-id="4be27-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4be27-127">Ignore</span></span>
- <span data-ttu-id="4be27-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4be27-128">Inquire</span></span>
- <span data-ttu-id="4be27-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4be27-129">SilentlyContinue</span></span>
- <span data-ttu-id="4be27-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="4be27-130">Stop</span></span>
- <span data-ttu-id="4be27-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4be27-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be27-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4be27-132">-InformationVariable</span></span>
<span data-ttu-id="4be27-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4be27-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be27-134">-Name</span><span class="sxs-lookup"><span data-stu-id="4be27-134">-Name</span></span>
<span data-ttu-id="4be27-135">Gibt den Namen der Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4be27-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be27-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="4be27-136">-Pre</span></span>
<span data-ttu-id="4be27-137">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4be27-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4be27-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be27-138">CommonParameters</span></span>
<span data-ttu-id="4be27-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be27-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be27-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be27-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be27-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4be27-141">INPUTS</span></span>

### <span data-ttu-id="4be27-142">Keine</span><span class="sxs-lookup"><span data-stu-id="4be27-142">None</span></span>
<span data-ttu-id="4be27-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4be27-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4be27-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4be27-144">OUTPUTS</span></span>

### <span data-ttu-id="4be27-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4be27-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4be27-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="4be27-146">NOTES</span></span>

## <span data-ttu-id="4be27-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4be27-147">RELATED LINKS</span></span>

[<span data-ttu-id="4be27-148">Neu – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4be27-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4be27-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4be27-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4be27-150">Satz-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4be27-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


