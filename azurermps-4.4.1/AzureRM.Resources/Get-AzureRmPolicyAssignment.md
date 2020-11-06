---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481610"
---
# <span data-ttu-id="1cd5c-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cd5c-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="1cd5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd5c-103">Ruft Richtlinienzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cd5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cd5c-104">SYNTAX</span></span>

### <span data-ttu-id="1cd5c-105">Der Parametersatz "alle Richtlinienzuweisungen auflisten"</span><span class="sxs-lookup"><span data-stu-id="1cd5c-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="1cd5c-106">Standard</span><span class="sxs-lookup"><span data-stu-id="1cd5c-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1cd5c-107">Der Parametersatz für den Richtlinien Zuordnungsnamen.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1cd5c-108">Der Parametersatz für die Richtlinien Zuweisungs-ID.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1cd5c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cd5c-109">DESCRIPTION</span></span>
<span data-ttu-id="1cd5c-110">Das Cmdlet " **Get-AzureRmPolicyAssignment** " ruft alle Richtlinienzuweisungen oder bestimmte Aufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="1cd5c-111">Identifizieren Sie eine Richtlinien Aufgabe, die nach Name und Bereich oder nach ID abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="1cd5c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cd5c-112">EXAMPLES</span></span>

### <span data-ttu-id="1cd5c-113">Beispiel 1: Abrufen aller Richtlinienzuweisungen</span><span class="sxs-lookup"><span data-stu-id="1cd5c-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="1cd5c-114">Mit diesem Befehl werden alle Richtlinienzuweisungen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="1cd5c-115">Beispiel 2: Abrufen einer bestimmten Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="1cd5c-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="1cd5c-116">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="1cd5c-117">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="1cd5c-118">Der zweite Befehl erhält die Richtlinienzuweisung mit dem Namen "PolicyAssignment07" für den Bereich, der von der Eigenschaft " **imsourcen** " von $ResourceGroup identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="1cd5c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cd5c-119">PARAMETERS</span></span>

### <span data-ttu-id="1cd5c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1cd5c-120">-ApiVersion</span></span>
<span data-ttu-id="1cd5c-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1cd5c-122">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1cd5c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="1cd5c-123">-Id</span></span>
<span data-ttu-id="1cd5c-124">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd5c-125">-Information</span><span class="sxs-lookup"><span data-stu-id="1cd5c-125">-InformationAction</span></span>
<span data-ttu-id="1cd5c-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1cd5c-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1cd5c-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1cd5c-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1cd5c-128">Continue</span></span>
- <span data-ttu-id="1cd5c-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1cd5c-129">Ignore</span></span>
- <span data-ttu-id="1cd5c-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1cd5c-130">Inquire</span></span>
- <span data-ttu-id="1cd5c-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1cd5c-131">SilentlyContinue</span></span>
- <span data-ttu-id="1cd5c-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="1cd5c-132">Stop</span></span>
- <span data-ttu-id="1cd5c-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1cd5c-133">Suspend</span></span>

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

### <span data-ttu-id="1cd5c-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1cd5c-134">-InformationVariable</span></span>
<span data-ttu-id="1cd5c-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1cd5c-136">-Name</span><span class="sxs-lookup"><span data-stu-id="1cd5c-136">-Name</span></span>
<span data-ttu-id="1cd5c-137">Gibt den Namen der Richtlinien Aufgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd5c-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1cd5c-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="1cd5c-139">Gibt die ID der Richtliniendefinition für die Richtlinienzuweisungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd5c-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="1cd5c-140">-Pre</span></span>
<span data-ttu-id="1cd5c-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1cd5c-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="1cd5c-142">-Scope</span></span>
<span data-ttu-id="1cd5c-143">Gibt den Bereich an, auf dem die Richtlinie für die Aufgabe angewendet wird, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd5c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd5c-144">-DefaultProfile</span></span>
<span data-ttu-id="1cd5c-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cd5c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd5c-146">CommonParameters</span></span>
<span data-ttu-id="1cd5c-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cd5c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd5c-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cd5c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd5c-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cd5c-149">INPUTS</span></span>

## <span data-ttu-id="1cd5c-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cd5c-150">OUTPUTS</span></span>

### <span data-ttu-id="1cd5c-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1cd5c-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1cd5c-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cd5c-152">NOTES</span></span>

## <span data-ttu-id="1cd5c-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cd5c-153">RELATED LINKS</span></span>

[<span data-ttu-id="1cd5c-154">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cd5c-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="1cd5c-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cd5c-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="1cd5c-156">Satz-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cd5c-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


