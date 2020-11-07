---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: ba2d158257f4be0e0daac8de5dd77e906e0abedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848647"
---
# <span data-ttu-id="110b1-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="110b1-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="110b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="110b1-102">SYNOPSIS</span></span>
<span data-ttu-id="110b1-103">Aktualisierung der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="110b1-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="110b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="110b1-104">SYNTAX</span></span>

### <span data-ttu-id="110b1-105">SetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="110b1-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="110b1-106">SetById</span><span class="sxs-lookup"><span data-stu-id="110b1-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="110b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="110b1-107">DESCRIPTION</span></span>
<span data-ttu-id="110b1-108">Das Cmdlet " **Satz-AzureRmManagedApplicationDefinition** " aktualisiert verwaltete Anwendungsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="110b1-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="110b1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="110b1-109">EXAMPLES</span></span>

### <span data-ttu-id="110b1-110">Beispiel 1: Aktualisieren der Definitionsbeschreibung für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="110b1-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="110b1-111">Dieser Befehl aktualisiert die Definitionsbeschreibung der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="110b1-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="110b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="110b1-112">PARAMETERS</span></span>

### <span data-ttu-id="110b1-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="110b1-113">-ApiVersion</span></span>
<span data-ttu-id="110b1-114">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="110b1-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="110b1-115">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="110b1-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="110b1-116">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="110b1-116">-Authorization</span></span>
<span data-ttu-id="110b1-117">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="110b1-117">The managed application definition authorization.</span></span>
<span data-ttu-id="110b1-118">Durch trennzeichengetrennte Autorisierungs Paare im Format \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="110b1-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110b1-119">-DefaultProfile</span></span>
<span data-ttu-id="110b1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="110b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="110b1-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="110b1-121">-Description</span></span>
<span data-ttu-id="110b1-122">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="110b1-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="110b1-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="110b1-123">-DisplayName</span></span>
<span data-ttu-id="110b1-124">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="110b1-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="110b1-125">-ID</span><span class="sxs-lookup"><span data-stu-id="110b1-125">-Id</span></span>
<span data-ttu-id="110b1-126">Die vollqualifizierte Definitions-ID der verwalteten Anwendung einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="110b1-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="110b1-127">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110b1-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110b1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="110b1-128">-Name</span></span>
<span data-ttu-id="110b1-129">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="110b1-129">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110b1-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="110b1-130">-PackageFileUri</span></span>
<span data-ttu-id="110b1-131">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="110b1-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="110b1-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="110b1-132">-Pre</span></span>
<span data-ttu-id="110b1-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="110b1-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="110b1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110b1-134">-ResourceGroupName</span></span>
<span data-ttu-id="110b1-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="110b1-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110b1-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="110b1-136">-Tag</span></span>
<span data-ttu-id="110b1-137">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="110b1-137">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="110b1-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="110b1-138">-Confirm</span></span>
<span data-ttu-id="110b1-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="110b1-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110b1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="110b1-140">-WhatIf</span></span>
<span data-ttu-id="110b1-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="110b1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="110b1-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="110b1-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110b1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110b1-143">CommonParameters</span></span>
<span data-ttu-id="110b1-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="110b1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110b1-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="110b1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110b1-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="110b1-146">INPUTS</span></span>

### <span data-ttu-id="110b1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="110b1-147">System.String</span></span>
<span data-ttu-id="110b1-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="110b1-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="110b1-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="110b1-149">OUTPUTS</span></span>

### <span data-ttu-id="110b1-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="110b1-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="110b1-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="110b1-151">NOTES</span></span>

## <span data-ttu-id="110b1-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="110b1-152">RELATED LINKS</span></span>
