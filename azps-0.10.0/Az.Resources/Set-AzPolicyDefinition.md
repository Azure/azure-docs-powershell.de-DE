---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: feddd9645b22c554d5e78813194ecc8837fdf3fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843195"
---
# <span data-ttu-id="d85b7-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d85b7-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="d85b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d85b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d85b7-103">Ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="d85b7-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="d85b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d85b7-104">SYNTAX</span></span>

### <span data-ttu-id="d85b7-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d85b7-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d85b7-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d85b7-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d85b7-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d85b7-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d85b7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d85b7-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d85b7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d85b7-109">DESCRIPTION</span></span>
<span data-ttu-id="d85b7-110">Das Cmdlet " **Satz-AzPolicyDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="d85b7-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="d85b7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d85b7-111">EXAMPLES</span></span>

### <span data-ttu-id="d85b7-112">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="d85b7-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="d85b7-113">Der erste Befehl ruft mithilfe des Get-AzPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="d85b7-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="d85b7-114">Der Befehl speichert das Objekt in der $PolicyDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="d85b7-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="d85b7-115">Der zweite Befehl aktualisiert die Beschreibung der Richtliniendefinition, die von der Eigenschaft " **Resourcen** -Eigenschaft" von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="d85b7-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="d85b7-116">Beispiel 2: Aktualisieren des Modus einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="d85b7-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="d85b7-117">Dieser Befehl aktualisiert die Richtliniendefinition mit dem Namen VMPolicyDefinition mithilfe des Set-AzPolicyDefinition-Cmdlets, um die Mode-Eigenschaft auf "alle" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d85b7-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="d85b7-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d85b7-118">PARAMETERS</span></span>

### <span data-ttu-id="d85b7-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d85b7-119">-ApiVersion</span></span>
<span data-ttu-id="d85b7-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="d85b7-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d85b7-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="d85b7-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d85b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85b7-122">-DefaultProfile</span></span>
<span data-ttu-id="d85b7-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d85b7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d85b7-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d85b7-124">-Description</span></span>
<span data-ttu-id="d85b7-125">Gibt eine neue Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="d85b7-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="d85b7-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d85b7-126">-DisplayName</span></span>
<span data-ttu-id="d85b7-127">Gibt einen neuen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="d85b7-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="d85b7-128">-ID</span><span class="sxs-lookup"><span data-stu-id="d85b7-128">-Id</span></span>
<span data-ttu-id="d85b7-129">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d85b7-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d85b7-130">-Information</span><span class="sxs-lookup"><span data-stu-id="d85b7-130">-InformationAction</span></span>
<span data-ttu-id="d85b7-131">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d85b7-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d85b7-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d85b7-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d85b7-133">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d85b7-133">Continue</span></span>
- <span data-ttu-id="d85b7-134">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d85b7-134">Ignore</span></span>
- <span data-ttu-id="d85b7-135">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d85b7-135">Inquire</span></span>
- <span data-ttu-id="d85b7-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d85b7-136">SilentlyContinue</span></span>
- <span data-ttu-id="d85b7-137">Beenden</span><span class="sxs-lookup"><span data-stu-id="d85b7-137">Stop</span></span>
- <span data-ttu-id="d85b7-138">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d85b7-138">Suspend</span></span>

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

### <span data-ttu-id="d85b7-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d85b7-139">-InformationVariable</span></span>
<span data-ttu-id="d85b7-140">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d85b7-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d85b7-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d85b7-141">-ManagementGroupName</span></span>
<span data-ttu-id="d85b7-142">Der Name der Verwaltungsgruppe der Richtliniendefinition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d85b7-142">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d85b7-143">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="d85b7-143">-Metadata</span></span>
<span data-ttu-id="d85b7-144">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="d85b7-144">The metadata for policy definition.</span></span> <span data-ttu-id="d85b7-145">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d85b7-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="d85b7-146">-Modus</span><span class="sxs-lookup"><span data-stu-id="d85b7-146">-Mode</span></span>
<span data-ttu-id="d85b7-147">Der Modus der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="d85b7-147">The mode of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d85b7-148">-Name</span><span class="sxs-lookup"><span data-stu-id="d85b7-148">-Name</span></span>
<span data-ttu-id="d85b7-149">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d85b7-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d85b7-150">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d85b7-150">-Parameter</span></span>
<span data-ttu-id="d85b7-151">Die Parameters-Deklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="d85b7-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d85b7-152">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d85b7-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d85b7-153">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d85b7-153">-Policy</span></span>
<span data-ttu-id="d85b7-154">Gibt neue Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="d85b7-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="d85b7-155">Sie können den Pfad einer JSON-Datei oder einer Zeichenfolge, die die Richtlinie enthält, im JSON-Format (JavaScript Object Notation) angeben.</span><span class="sxs-lookup"><span data-stu-id="d85b7-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="d85b7-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="d85b7-156">-Pre</span></span>
<span data-ttu-id="d85b7-157">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d85b7-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d85b7-158">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d85b7-158">-SubscriptionId</span></span>
<span data-ttu-id="d85b7-159">Die Abonnement-ID der Richtliniendefinition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d85b7-159">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d85b7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85b7-160">CommonParameters</span></span>
<span data-ttu-id="d85b7-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85b7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85b7-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d85b7-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85b7-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d85b7-163">INPUTS</span></span>

## <span data-ttu-id="d85b7-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d85b7-164">OUTPUTS</span></span>

## <span data-ttu-id="d85b7-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="d85b7-165">NOTES</span></span>

## <span data-ttu-id="d85b7-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d85b7-166">RELATED LINKS</span></span>

[<span data-ttu-id="d85b7-167">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d85b7-167">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="d85b7-168">Neu – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d85b7-168">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="d85b7-169">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d85b7-169">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


