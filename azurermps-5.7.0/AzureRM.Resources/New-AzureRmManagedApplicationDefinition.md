---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 5574966734c3b35bd5b104addf1872a85eb9660b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482738"
---
# <span data-ttu-id="f2663-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f2663-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="f2663-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2663-102">SYNOPSIS</span></span>
<span data-ttu-id="f2663-103">Erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="f2663-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2663-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2663-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2663-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2663-105">DESCRIPTION</span></span>
<span data-ttu-id="f2663-106">Das Cmdlet **New-AzureRmManagedApplicationDefinition** erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="f2663-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="f2663-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2663-107">EXAMPLES</span></span>

### <span data-ttu-id="f2663-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2663-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="f2663-109">Mit diesem Befehl wird eine verwaltete Anwendungsdefinition erstellt</span><span class="sxs-lookup"><span data-stu-id="f2663-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="f2663-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2663-110">PARAMETERS</span></span>

### <span data-ttu-id="f2663-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f2663-111">-ApiVersion</span></span>
<span data-ttu-id="f2663-112">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2663-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f2663-113">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f2663-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f2663-114">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="f2663-114">-Authorization</span></span>
<span data-ttu-id="f2663-115">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="f2663-115">The managed application definition authorization.</span></span>
<span data-ttu-id="f2663-116">Durch trennzeichengetrennte Autorisierungs Paare im Format \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="f2663-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2663-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="f2663-117">-CreateUiDefinition</span></span>
<span data-ttu-id="f2663-118">Definition der verwalteten Anwendung erstellen einer UI-Definition</span><span class="sxs-lookup"><span data-stu-id="f2663-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="f2663-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2663-119">-DefaultProfile</span></span>
<span data-ttu-id="f2663-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2663-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2663-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2663-121">-Description</span></span>
<span data-ttu-id="f2663-122">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="f2663-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="f2663-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2663-123">-DisplayName</span></span>
<span data-ttu-id="f2663-124">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="f2663-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="f2663-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="f2663-125">-Location</span></span>
<span data-ttu-id="f2663-126">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f2663-126">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2663-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="f2663-127">-LockLevel</span></span>
<span data-ttu-id="f2663-128">Die Ebene der Sperre für die Definition einer verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f2663-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2663-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="f2663-129">-MainTemplate</span></span>
<span data-ttu-id="f2663-130">Hauptvorlage für die verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="f2663-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="f2663-131">-Name</span><span class="sxs-lookup"><span data-stu-id="f2663-131">-Name</span></span>
<span data-ttu-id="f2663-132">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f2663-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="f2663-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="f2663-133">-PackageFileUri</span></span>
<span data-ttu-id="f2663-134">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="f2663-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="f2663-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2663-135">-Pre</span></span>
<span data-ttu-id="f2663-136">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f2663-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f2663-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2663-137">-ResourceGroupName</span></span>
<span data-ttu-id="f2663-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2663-138">The resource group name.</span></span>

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

### <span data-ttu-id="f2663-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2663-139">-Tag</span></span>
<span data-ttu-id="f2663-140">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2663-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f2663-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2663-141">-Confirm</span></span>
<span data-ttu-id="f2663-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2663-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2663-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2663-143">-WhatIf</span></span>
<span data-ttu-id="f2663-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2663-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2663-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2663-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2663-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2663-146">CommonParameters</span></span>
<span data-ttu-id="f2663-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2663-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2663-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2663-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2663-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2663-149">INPUTS</span></span>

### <span data-ttu-id="f2663-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f2663-150">System.String</span></span>
<span data-ttu-id="f2663-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2663-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2663-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2663-152">OUTPUTS</span></span>

### <span data-ttu-id="f2663-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f2663-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f2663-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2663-154">NOTES</span></span>

## <span data-ttu-id="f2663-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2663-155">RELATED LINKS</span></span>
