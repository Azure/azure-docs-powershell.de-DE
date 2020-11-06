---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501405"
---
# <span data-ttu-id="19126-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19126-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="19126-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19126-102">SYNOPSIS</span></span>
<span data-ttu-id="19126-103">Ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="19126-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19126-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19126-104">SYNTAX</span></span>

### <span data-ttu-id="19126-105">SetByPolicyDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="19126-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="19126-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="19126-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="19126-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="19126-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="19126-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19126-108">DESCRIPTION</span></span>
<span data-ttu-id="19126-109">Das Cmdlet " **Satz-AzureRmPolicyDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="19126-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="19126-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19126-110">EXAMPLES</span></span>

### <span data-ttu-id="19126-111">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="19126-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="19126-112">Der erste Befehl ruft mithilfe des Get-AzureRmPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="19126-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="19126-113">Der Befehl speichert das Objekt in der $PolicyDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="19126-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="19126-114">Der zweite Befehl aktualisiert die Beschreibung der Richtliniendefinition, die von der Eigenschaft " **Resourcen** -Eigenschaft" von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="19126-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="19126-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="19126-115">PARAMETERS</span></span>

### <span data-ttu-id="19126-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19126-116">-ApiVersion</span></span>
<span data-ttu-id="19126-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="19126-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="19126-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="19126-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="19126-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19126-119">-DefaultProfile</span></span>
<span data-ttu-id="19126-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="19126-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19126-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19126-121">-Description</span></span>
<span data-ttu-id="19126-122">Gibt eine neue Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="19126-122">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="19126-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="19126-123">-DisplayName</span></span>
<span data-ttu-id="19126-124">Gibt einen neuen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="19126-124">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="19126-125">-ID</span><span class="sxs-lookup"><span data-stu-id="19126-125">-Id</span></span>
<span data-ttu-id="19126-126">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="19126-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="19126-127">-Information</span><span class="sxs-lookup"><span data-stu-id="19126-127">-InformationAction</span></span>
<span data-ttu-id="19126-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="19126-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19126-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="19126-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19126-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="19126-130">Continue</span></span>
- <span data-ttu-id="19126-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="19126-131">Ignore</span></span>
- <span data-ttu-id="19126-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="19126-132">Inquire</span></span>
- <span data-ttu-id="19126-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="19126-133">SilentlyContinue</span></span>
- <span data-ttu-id="19126-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="19126-134">Stop</span></span>
- <span data-ttu-id="19126-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="19126-135">Suspend</span></span>

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

### <span data-ttu-id="19126-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="19126-136">-InformationVariable</span></span>
<span data-ttu-id="19126-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="19126-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="19126-138">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="19126-138">-Metadata</span></span>
<span data-ttu-id="19126-139">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="19126-139">The metadata for policy definition.</span></span> <span data-ttu-id="19126-140">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="19126-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="19126-141">-Name</span><span class="sxs-lookup"><span data-stu-id="19126-141">-Name</span></span>
<span data-ttu-id="19126-142">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="19126-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="19126-143">-Parameter</span><span class="sxs-lookup"><span data-stu-id="19126-143">-Parameter</span></span>
<span data-ttu-id="19126-144">Die Parameters-Deklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="19126-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="19126-145">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="19126-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="19126-146">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="19126-146">-Policy</span></span>
<span data-ttu-id="19126-147">Gibt neue Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="19126-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="19126-148">Sie können den Pfad einer JSON-Datei oder einer Zeichenfolge, die die Richtlinie enthält, im JSON-Format (JavaScript Object Notation) angeben.</span><span class="sxs-lookup"><span data-stu-id="19126-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="19126-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="19126-149">-Pre</span></span>
<span data-ttu-id="19126-150">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="19126-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="19126-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19126-151">CommonParameters</span></span>
<span data-ttu-id="19126-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19126-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19126-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19126-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19126-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19126-154">INPUTS</span></span>

### <span data-ttu-id="19126-155">Keine</span><span class="sxs-lookup"><span data-stu-id="19126-155">None</span></span>
<span data-ttu-id="19126-156">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="19126-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19126-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19126-157">OUTPUTS</span></span>

### <span data-ttu-id="19126-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="19126-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19126-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="19126-159">NOTES</span></span>

## <span data-ttu-id="19126-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19126-160">RELATED LINKS</span></span>

[<span data-ttu-id="19126-161">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19126-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="19126-162">Neu – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19126-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="19126-163">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19126-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


