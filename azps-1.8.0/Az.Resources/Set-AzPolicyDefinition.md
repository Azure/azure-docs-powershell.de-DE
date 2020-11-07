---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: f96ea5b7f36806378dff31cc81d211074638342c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659521"
---
# <span data-ttu-id="75ff8-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="75ff8-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="75ff8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="75ff8-103">Ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="75ff8-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="75ff8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75ff8-104">SYNTAX</span></span>

### <span data-ttu-id="75ff8-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="75ff8-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75ff8-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75ff8-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75ff8-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75ff8-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75ff8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75ff8-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75ff8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75ff8-109">DESCRIPTION</span></span>
<span data-ttu-id="75ff8-110">Das Cmdlet " **Satz-AzPolicyDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="75ff8-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="75ff8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75ff8-111">EXAMPLES</span></span>

### <span data-ttu-id="75ff8-112">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="75ff8-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="75ff8-113">Der erste Befehl ruft mithilfe des Get-AzPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="75ff8-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="75ff8-114">Der Befehl speichert das Objekt in der $PolicyDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="75ff8-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="75ff8-115">Der zweite Befehl aktualisiert die Beschreibung der Richtliniendefinition, die von der Eigenschaft " **Resourcen** -Eigenschaft" von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="75ff8-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="75ff8-116">Beispiel 2: Aktualisieren des Modus einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="75ff8-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="75ff8-117">Dieser Befehl aktualisiert die Richtliniendefinition mit dem Namen VMPolicyDefinition mithilfe des Set-AzPolicyDefinition-Cmdlets, um die Mode-Eigenschaft auf "alle" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="75ff8-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="75ff8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="75ff8-118">PARAMETERS</span></span>

### <span data-ttu-id="75ff8-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="75ff8-119">-ApiVersion</span></span>
<span data-ttu-id="75ff8-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="75ff8-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="75ff8-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="75ff8-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="75ff8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ff8-122">-DefaultProfile</span></span>
<span data-ttu-id="75ff8-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75ff8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75ff8-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75ff8-124">-Description</span></span>
<span data-ttu-id="75ff8-125">Gibt eine neue Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="75ff8-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="75ff8-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75ff8-126">-DisplayName</span></span>
<span data-ttu-id="75ff8-127">Gibt einen neuen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="75ff8-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="75ff8-128">-ID</span><span class="sxs-lookup"><span data-stu-id="75ff8-128">-Id</span></span>
<span data-ttu-id="75ff8-129">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="75ff8-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="75ff8-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="75ff8-130">-ManagementGroupName</span></span>
<span data-ttu-id="75ff8-131">Der Name der Verwaltungsgruppe der Richtliniendefinition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="75ff8-131">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="75ff8-132">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="75ff8-132">-Metadata</span></span>
<span data-ttu-id="75ff8-133">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="75ff8-133">The metadata for policy definition.</span></span> <span data-ttu-id="75ff8-134">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="75ff8-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="75ff8-135">-Modus</span><span class="sxs-lookup"><span data-stu-id="75ff8-135">-Mode</span></span>
<span data-ttu-id="75ff8-136">Der Modus der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="75ff8-136">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="75ff8-137">-Name</span><span class="sxs-lookup"><span data-stu-id="75ff8-137">-Name</span></span>
<span data-ttu-id="75ff8-138">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="75ff8-138">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="75ff8-139">-Parameter</span><span class="sxs-lookup"><span data-stu-id="75ff8-139">-Parameter</span></span>
<span data-ttu-id="75ff8-140">Die Parameters-Deklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="75ff8-140">The parameters declaration for policy definition.</span></span> <span data-ttu-id="75ff8-141">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="75ff8-141">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="75ff8-142">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="75ff8-142">-Policy</span></span>
<span data-ttu-id="75ff8-143">Gibt neue Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="75ff8-143">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="75ff8-144">Sie können den Pfad einer JSON-Datei oder einer Zeichenfolge, die die Richtlinie enthält, im JSON-Format (JavaScript Object Notation) angeben.</span><span class="sxs-lookup"><span data-stu-id="75ff8-144">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="75ff8-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="75ff8-145">-Pre</span></span>
<span data-ttu-id="75ff8-146">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="75ff8-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="75ff8-147">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="75ff8-147">-SubscriptionId</span></span>
<span data-ttu-id="75ff8-148">Die Abonnement-ID der Richtliniendefinition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="75ff8-148">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="75ff8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ff8-149">CommonParameters</span></span>
<span data-ttu-id="75ff8-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ff8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ff8-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ff8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ff8-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75ff8-152">INPUTS</span></span>

### <span data-ttu-id="75ff8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="75ff8-153">System.String</span></span>

### <span data-ttu-id="75ff8-154">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75ff8-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="75ff8-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75ff8-155">OUTPUTS</span></span>

### <span data-ttu-id="75ff8-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="75ff8-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="75ff8-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="75ff8-157">NOTES</span></span>

## <span data-ttu-id="75ff8-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75ff8-158">RELATED LINKS</span></span>

[<span data-ttu-id="75ff8-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="75ff8-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="75ff8-160">Neu – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="75ff8-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="75ff8-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="75ff8-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


