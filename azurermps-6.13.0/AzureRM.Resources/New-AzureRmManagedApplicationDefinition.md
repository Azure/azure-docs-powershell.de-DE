---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ebabe915fd203ffd73c111b0be5a2e82e2bea3a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475937"
---
# <span data-ttu-id="0e403-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="0e403-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="0e403-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e403-102">SYNOPSIS</span></span>
<span data-ttu-id="0e403-103">Erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="0e403-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e403-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e403-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e403-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e403-105">DESCRIPTION</span></span>
<span data-ttu-id="0e403-106">Das Cmdlet **New-AzureRmManagedApplicationDefinition** erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="0e403-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="0e403-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e403-107">EXAMPLES</span></span>

### <span data-ttu-id="0e403-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e403-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="0e403-109">Mit diesem Befehl wird eine verwaltete Anwendungsdefinition erstellt</span><span class="sxs-lookup"><span data-stu-id="0e403-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="0e403-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e403-110">PARAMETERS</span></span>

### <span data-ttu-id="0e403-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0e403-111">-ApiVersion</span></span>
<span data-ttu-id="0e403-112">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e403-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0e403-113">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0e403-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0e403-114">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="0e403-114">-Authorization</span></span>
<span data-ttu-id="0e403-115">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="0e403-115">The managed application definition authorization.</span></span>
<span data-ttu-id="0e403-116">Durch trennzeichengetrennte Autorisierungs Paare im Format \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="0e403-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e403-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="0e403-117">-CreateUiDefinition</span></span>
<span data-ttu-id="0e403-118">Definition der verwalteten Anwendung erstellen einer UI-Definition</span><span class="sxs-lookup"><span data-stu-id="0e403-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="0e403-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e403-119">-DefaultProfile</span></span>
<span data-ttu-id="0e403-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e403-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e403-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e403-121">-Description</span></span>
<span data-ttu-id="0e403-122">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="0e403-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e403-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0e403-123">-DisplayName</span></span>
<span data-ttu-id="0e403-124">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="0e403-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e403-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="0e403-125">-Location</span></span>
<span data-ttu-id="0e403-126">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0e403-126">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e403-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="0e403-127">-LockLevel</span></span>
<span data-ttu-id="0e403-128">Die Ebene der Sperre für die Definition einer verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0e403-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e403-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="0e403-129">-MainTemplate</span></span>
<span data-ttu-id="0e403-130">Hauptvorlage für die verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="0e403-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="0e403-131">-Name</span><span class="sxs-lookup"><span data-stu-id="0e403-131">-Name</span></span>
<span data-ttu-id="0e403-132">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0e403-132">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e403-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="0e403-133">-PackageFileUri</span></span>
<span data-ttu-id="0e403-134">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="0e403-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="0e403-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="0e403-135">-Pre</span></span>
<span data-ttu-id="0e403-136">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="0e403-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0e403-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e403-137">-ResourceGroupName</span></span>
<span data-ttu-id="0e403-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e403-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e403-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e403-139">-Tag</span></span>
<span data-ttu-id="0e403-140">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e403-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0e403-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e403-141">-Confirm</span></span>
<span data-ttu-id="0e403-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e403-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e403-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e403-143">-WhatIf</span></span>
<span data-ttu-id="0e403-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e403-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e403-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e403-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e403-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e403-146">CommonParameters</span></span>
<span data-ttu-id="0e403-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e403-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e403-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e403-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e403-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e403-149">INPUTS</span></span>

### <span data-ttu-id="0e403-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0e403-150">System.String</span></span>

### <span data-ttu-id="0e403-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="0e403-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="0e403-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="0e403-152">System.String[]</span></span>

### <span data-ttu-id="0e403-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e403-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0e403-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e403-154">OUTPUTS</span></span>

### <span data-ttu-id="0e403-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0e403-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0e403-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e403-156">NOTES</span></span>

## <span data-ttu-id="0e403-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e403-157">RELATED LINKS</span></span>
