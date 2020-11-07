---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664442"
---
# <span data-ttu-id="24d2b-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24d2b-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="24d2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="24d2b-103">Ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="24d2b-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24d2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24d2b-104">SYNTAX</span></span>

### <span data-ttu-id="24d2b-105">Der Parametersatz für den Richtlinien Definitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="24d2b-105">The policy definition name parameter set.</span></span> <span data-ttu-id="24d2b-106">Standard</span><span class="sxs-lookup"><span data-stu-id="24d2b-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="24d2b-107">Der Parametersatz für die Richtlinien Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="24d2b-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="24d2b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24d2b-108">DESCRIPTION</span></span>
<span data-ttu-id="24d2b-109">Das Cmdlet " **Satz-AzureRmPolicyDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="24d2b-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="24d2b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24d2b-110">EXAMPLES</span></span>

### <span data-ttu-id="24d2b-111">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="24d2b-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="24d2b-112">Der erste Befehl ruft mithilfe des Get-AzureRmPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="24d2b-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="24d2b-113">Der Befehl speichert das Objekt in der $PolicyDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="24d2b-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="24d2b-114">Der zweite Befehl aktualisiert die Beschreibung der Richtliniendefinition, die von der Eigenschaft " **Resourcen** -Eigenschaft" von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="24d2b-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="24d2b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="24d2b-115">PARAMETERS</span></span>

### <span data-ttu-id="24d2b-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="24d2b-116">-ApiVersion</span></span>
<span data-ttu-id="24d2b-117">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="24d2b-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="24d2b-118">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="24d2b-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="24d2b-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24d2b-119">-Description</span></span>
<span data-ttu-id="24d2b-120">Gibt eine neue Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="24d2b-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="24d2b-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="24d2b-121">-DisplayName</span></span>
<span data-ttu-id="24d2b-122">Gibt einen neuen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="24d2b-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="24d2b-123">-ID</span><span class="sxs-lookup"><span data-stu-id="24d2b-123">-Id</span></span>
<span data-ttu-id="24d2b-124">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="24d2b-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="24d2b-125">-Information</span><span class="sxs-lookup"><span data-stu-id="24d2b-125">-InformationAction</span></span>
<span data-ttu-id="24d2b-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="24d2b-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="24d2b-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="24d2b-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24d2b-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="24d2b-128">Continue</span></span>
- <span data-ttu-id="24d2b-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="24d2b-129">Ignore</span></span>
- <span data-ttu-id="24d2b-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="24d2b-130">Inquire</span></span>
- <span data-ttu-id="24d2b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="24d2b-131">SilentlyContinue</span></span>
- <span data-ttu-id="24d2b-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="24d2b-132">Stop</span></span>
- <span data-ttu-id="24d2b-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="24d2b-133">Suspend</span></span>

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

### <span data-ttu-id="24d2b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="24d2b-134">-InformationVariable</span></span>
<span data-ttu-id="24d2b-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="24d2b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="24d2b-136">-Name</span><span class="sxs-lookup"><span data-stu-id="24d2b-136">-Name</span></span>
<span data-ttu-id="24d2b-137">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="24d2b-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="24d2b-138">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="24d2b-138">-Policy</span></span>
<span data-ttu-id="24d2b-139">Gibt neue Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="24d2b-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="24d2b-140">Sie können den Pfad einer JSON-Datei oder einer Zeichenfolge, die die Richtlinie enthält, im JSON-Format (JavaScript Object Notation) angeben.</span><span class="sxs-lookup"><span data-stu-id="24d2b-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="24d2b-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="24d2b-141">-Pre</span></span>
<span data-ttu-id="24d2b-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="24d2b-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="24d2b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d2b-143">-DefaultProfile</span></span>
<span data-ttu-id="24d2b-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24d2b-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24d2b-145">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="24d2b-145">-Metadata</span></span>
<span data-ttu-id="24d2b-146">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="24d2b-146">The metadata for policy definition.</span></span> <span data-ttu-id="24d2b-147">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24d2b-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="24d2b-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="24d2b-148">-Parameter</span></span>
<span data-ttu-id="24d2b-149">Die Parameters-Deklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="24d2b-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="24d2b-150">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="24d2b-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="24d2b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d2b-151">CommonParameters</span></span>
<span data-ttu-id="24d2b-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d2b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d2b-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d2b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d2b-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24d2b-154">INPUTS</span></span>

## <span data-ttu-id="24d2b-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24d2b-155">OUTPUTS</span></span>

### <span data-ttu-id="24d2b-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="24d2b-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="24d2b-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="24d2b-157">NOTES</span></span>

## <span data-ttu-id="24d2b-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24d2b-158">RELATED LINKS</span></span>

[<span data-ttu-id="24d2b-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24d2b-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="24d2b-160">Neu – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24d2b-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="24d2b-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24d2b-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


