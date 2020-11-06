---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 8914b6d48b14ea372f29a6b7b0f5c9a1c32a6fd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476605"
---
# <span data-ttu-id="d6def-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="d6def-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="d6def-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6def-102">SYNOPSIS</span></span>
<span data-ttu-id="d6def-103">Aktualisierung der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="d6def-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6def-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6def-104">SYNTAX</span></span>

### <span data-ttu-id="d6def-105">SetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6def-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6def-106">SetById</span><span class="sxs-lookup"><span data-stu-id="d6def-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6def-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6def-107">DESCRIPTION</span></span>
<span data-ttu-id="d6def-108">Das Cmdlet " **Satz-AzureRmManagedApplicationDefinition** " aktualisiert verwaltete Anwendungsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d6def-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="d6def-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6def-109">EXAMPLES</span></span>

### <span data-ttu-id="d6def-110">Beispiel 1: Aktualisieren der Definitionsbeschreibung für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d6def-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="d6def-111">Dieser Befehl aktualisiert die Definitionsbeschreibung der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d6def-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="d6def-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6def-112">PARAMETERS</span></span>

### <span data-ttu-id="d6def-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d6def-113">-ApiVersion</span></span>
<span data-ttu-id="d6def-114">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6def-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6def-115">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d6def-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d6def-116">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="d6def-116">-Authorization</span></span>
<span data-ttu-id="d6def-117">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d6def-117">The managed application definition authorization.</span></span>
<span data-ttu-id="d6def-118">Durch trennzeichengetrennte Autorisierungs Paare im Format \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="d6def-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="d6def-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6def-119">-DefaultProfile</span></span>
<span data-ttu-id="d6def-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6def-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6def-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6def-121">-Description</span></span>
<span data-ttu-id="d6def-122">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="d6def-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="d6def-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d6def-123">-DisplayName</span></span>
<span data-ttu-id="d6def-124">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="d6def-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="d6def-125">-ID</span><span class="sxs-lookup"><span data-stu-id="d6def-125">-Id</span></span>
<span data-ttu-id="d6def-126">Die vollqualifizierte Definitions-ID der verwalteten Anwendung einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="d6def-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="d6def-127">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6def-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="d6def-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d6def-128">-Name</span></span>
<span data-ttu-id="d6def-129">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d6def-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="d6def-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="d6def-130">-PackageFileUri</span></span>
<span data-ttu-id="d6def-131">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="d6def-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="d6def-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6def-132">-Pre</span></span>
<span data-ttu-id="d6def-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d6def-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d6def-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6def-134">-ResourceGroupName</span></span>
<span data-ttu-id="d6def-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d6def-135">The resource group name.</span></span>

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

### <span data-ttu-id="d6def-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6def-136">-Tag</span></span>
<span data-ttu-id="d6def-137">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="d6def-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="d6def-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6def-138">-Confirm</span></span>
<span data-ttu-id="d6def-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6def-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6def-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6def-140">-WhatIf</span></span>
<span data-ttu-id="d6def-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6def-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6def-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6def-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6def-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6def-143">CommonParameters</span></span>
<span data-ttu-id="d6def-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6def-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6def-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6def-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6def-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6def-146">INPUTS</span></span>

### <span data-ttu-id="d6def-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d6def-147">System.String</span></span>
<span data-ttu-id="d6def-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d6def-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="d6def-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6def-149">OUTPUTS</span></span>

### <span data-ttu-id="d6def-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d6def-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d6def-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6def-151">NOTES</span></span>

## <span data-ttu-id="d6def-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6def-152">RELATED LINKS</span></span>
