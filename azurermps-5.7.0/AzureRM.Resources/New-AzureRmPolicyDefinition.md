---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: e39d60863b9409a6d52f2f92dc312e98b8e50cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480966"
---
# <span data-ttu-id="eced5-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eced5-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="eced5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eced5-102">SYNOPSIS</span></span>
<span data-ttu-id="eced5-103">Erstellt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="eced5-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eced5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eced5-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eced5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eced5-105">DESCRIPTION</span></span>
<span data-ttu-id="eced5-106">Das Cmdlet **New-AzureRmPolicyDefinition** erstellt eine Richtliniendefinition, die eine Richtlinienregel im JSON-Format (JavaScript Object Notation) enthält.</span><span class="sxs-lookup"><span data-stu-id="eced5-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="eced5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eced5-107">EXAMPLES</span></span>

### <span data-ttu-id="eced5-108">Beispiel 1: Erstellen einer Richtliniendefinition mithilfe einer Richtliniendatei</span><span class="sxs-lookup"><span data-stu-id="eced5-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="eced5-109">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen VMPolicyDefinition erstellt, die die in C:\VMPolicy.json angegebene Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="eced5-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="eced5-110">Beispiel 2: Erstellen einer Richtliniendefinition Inline</span><span class="sxs-lookup"><span data-stu-id="eced5-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="eced5-111">Dieser Befehl erstellt eine Richtliniendefinition mit dem Namen VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="eced5-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="eced5-112">Der Befehl gibt die Richtlinie als Zeichenfolge im gültigen JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="eced5-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="eced5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="eced5-113">PARAMETERS</span></span>

### <span data-ttu-id="eced5-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eced5-114">-ApiVersion</span></span>
<span data-ttu-id="eced5-115">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="eced5-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="eced5-116">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="eced5-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="eced5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eced5-117">-DefaultProfile</span></span>
<span data-ttu-id="eced5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eced5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eced5-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eced5-119">-Description</span></span>
<span data-ttu-id="eced5-120">Gibt eine Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="eced5-120">Specifies a description for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eced5-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eced5-121">-DisplayName</span></span>
<span data-ttu-id="eced5-122">Gibt einen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="eced5-122">Specifies a display name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eced5-123">-Information</span><span class="sxs-lookup"><span data-stu-id="eced5-123">-InformationAction</span></span>
<span data-ttu-id="eced5-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="eced5-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eced5-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eced5-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eced5-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="eced5-126">Continue</span></span>
- <span data-ttu-id="eced5-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="eced5-127">Ignore</span></span>
- <span data-ttu-id="eced5-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="eced5-128">Inquire</span></span>
- <span data-ttu-id="eced5-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eced5-129">SilentlyContinue</span></span>
- <span data-ttu-id="eced5-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="eced5-130">Stop</span></span>
- <span data-ttu-id="eced5-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="eced5-131">Suspend</span></span>

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

### <span data-ttu-id="eced5-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eced5-132">-InformationVariable</span></span>
<span data-ttu-id="eced5-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="eced5-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eced5-134">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="eced5-134">-Metadata</span></span>
<span data-ttu-id="eced5-135">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="eced5-135">The metadata for policy definition.</span></span> <span data-ttu-id="eced5-136">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="eced5-136">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eced5-137">-Modus</span><span class="sxs-lookup"><span data-stu-id="eced5-137">-Mode</span></span>
<span data-ttu-id="eced5-138">Der Modus der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="eced5-138">The mode of the policy definition</span></span>

```yaml
Type: PolicyDefinitionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eced5-139">-Name</span><span class="sxs-lookup"><span data-stu-id="eced5-139">-Name</span></span>
<span data-ttu-id="eced5-140">Gibt einen Namen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="eced5-140">Specifies a name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eced5-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="eced5-141">-Parameter</span></span>
<span data-ttu-id="eced5-142">Die Parameters-Deklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="eced5-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="eced5-143">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="eced5-143">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eced5-144">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="eced5-144">-Policy</span></span>
<span data-ttu-id="eced5-145">Gibt eine Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="eced5-145">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="eced5-146">Sie können den Pfad einer JSON-Datei oder einer Zeichenfolge, die die Richtlinie enthält, im JSON-Format angeben.</span><span class="sxs-lookup"><span data-stu-id="eced5-146">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eced5-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="eced5-147">-Pre</span></span>
<span data-ttu-id="eced5-148">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="eced5-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="eced5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eced5-149">CommonParameters</span></span>
<span data-ttu-id="eced5-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eced5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eced5-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eced5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eced5-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eced5-152">INPUTS</span></span>

### <span data-ttu-id="eced5-153">Keine</span><span class="sxs-lookup"><span data-stu-id="eced5-153">None</span></span>
<span data-ttu-id="eced5-154">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="eced5-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eced5-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eced5-155">OUTPUTS</span></span>

### <span data-ttu-id="eced5-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="eced5-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eced5-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="eced5-157">NOTES</span></span>

## <span data-ttu-id="eced5-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eced5-158">RELATED LINKS</span></span>

[<span data-ttu-id="eced5-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eced5-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="eced5-160">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eced5-160">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="eced5-161">Satz-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eced5-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


