---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: d1da0ce7f8a88a12b0714960a60d5b2aa523a0a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659523"
---
# <span data-ttu-id="06a4b-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="06a4b-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="06a4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="06a4b-103">Aktualisierung der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="06a4b-103">Updates managed application definition</span></span>

## <span data-ttu-id="06a4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06a4b-104">SYNTAX</span></span>

### <span data-ttu-id="06a4b-105">SetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="06a4b-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06a4b-106">SetById</span><span class="sxs-lookup"><span data-stu-id="06a4b-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a4b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06a4b-107">DESCRIPTION</span></span>
<span data-ttu-id="06a4b-108">Das Cmdlet " **Satz-AzManagedApplicationDefinition** " aktualisiert verwaltete Anwendungsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="06a4b-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="06a4b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06a4b-109">EXAMPLES</span></span>

### <span data-ttu-id="06a4b-110">Beispiel 1: Aktualisieren der Definitionsbeschreibung für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="06a4b-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="06a4b-111">Dieser Befehl aktualisiert die Definitionsbeschreibung der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="06a4b-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="06a4b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="06a4b-112">PARAMETERS</span></span>

### <span data-ttu-id="06a4b-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06a4b-113">-ApiVersion</span></span>
<span data-ttu-id="06a4b-114">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06a4b-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="06a4b-115">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="06a4b-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="06a4b-116">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="06a4b-116">-Authorization</span></span>
<span data-ttu-id="06a4b-117">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="06a4b-117">The managed application definition authorization.</span></span>
<span data-ttu-id="06a4b-118">Durch trennzeichengetrennte Autorisierungs Paare im Format der Prinzipal-Nr \< \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="06a4b-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a4b-119">-DefaultProfile</span></span>
<span data-ttu-id="06a4b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06a4b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a4b-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06a4b-121">-Description</span></span>
<span data-ttu-id="06a4b-122">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="06a4b-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="06a4b-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="06a4b-123">-DisplayName</span></span>
<span data-ttu-id="06a4b-124">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="06a4b-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="06a4b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="06a4b-125">-Id</span></span>
<span data-ttu-id="06a4b-126">Die vollqualifizierte Definitions-ID der verwalteten Anwendung einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="06a4b-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="06a4b-127">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a4b-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a4b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="06a4b-128">-Name</span></span>
<span data-ttu-id="06a4b-129">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="06a4b-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a4b-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="06a4b-130">-PackageFileUri</span></span>
<span data-ttu-id="06a4b-131">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="06a4b-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="06a4b-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="06a4b-132">-Pre</span></span>
<span data-ttu-id="06a4b-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="06a4b-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="06a4b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a4b-134">-ResourceGroupName</span></span>
<span data-ttu-id="06a4b-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06a4b-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a4b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="06a4b-136">-Tag</span></span>
<span data-ttu-id="06a4b-137">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="06a4b-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a4b-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06a4b-138">-Confirm</span></span>
<span data-ttu-id="06a4b-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06a4b-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a4b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a4b-140">-WhatIf</span></span>
<span data-ttu-id="06a4b-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06a4b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a4b-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06a4b-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a4b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a4b-143">CommonParameters</span></span>
<span data-ttu-id="06a4b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a4b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a4b-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a4b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a4b-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06a4b-146">INPUTS</span></span>

### <span data-ttu-id="06a4b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="06a4b-147">System.String</span></span>

### <span data-ttu-id="06a4b-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="06a4b-148">System.String[]</span></span>

### <span data-ttu-id="06a4b-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06a4b-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06a4b-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06a4b-150">OUTPUTS</span></span>

### <span data-ttu-id="06a4b-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="06a4b-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06a4b-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="06a4b-152">NOTES</span></span>

## <span data-ttu-id="06a4b-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06a4b-153">RELATED LINKS</span></span>
