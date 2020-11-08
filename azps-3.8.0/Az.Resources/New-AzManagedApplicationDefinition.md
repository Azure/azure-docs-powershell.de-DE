---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003287"
---
# <span data-ttu-id="06b90-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="06b90-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="06b90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06b90-102">SYNOPSIS</span></span>
<span data-ttu-id="06b90-103">Erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="06b90-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="06b90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06b90-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06b90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06b90-105">DESCRIPTION</span></span>
<span data-ttu-id="06b90-106">Das Cmdlet **New-AzManagedApplicationDefinition** erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="06b90-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="06b90-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06b90-107">EXAMPLES</span></span>

### <span data-ttu-id="06b90-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06b90-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="06b90-109">Mit diesem Befehl wird eine verwaltete Anwendungsdefinition erstellt</span><span class="sxs-lookup"><span data-stu-id="06b90-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="06b90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="06b90-110">PARAMETERS</span></span>

### <span data-ttu-id="06b90-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06b90-111">-ApiVersion</span></span>
<span data-ttu-id="06b90-112">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06b90-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="06b90-113">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="06b90-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="06b90-114">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="06b90-114">-Authorization</span></span>
<span data-ttu-id="06b90-115">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="06b90-115">The managed application definition authorization.</span></span>
<span data-ttu-id="06b90-116">Durch trennzeichengetrennte Autorisierungs Paare im Format der Prinzipal-Nr \< \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="06b90-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="06b90-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="06b90-117">-CreateUiDefinition</span></span>
<span data-ttu-id="06b90-118">Definition der verwalteten Anwendung erstellen einer UI-Definition</span><span class="sxs-lookup"><span data-stu-id="06b90-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="06b90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b90-119">-DefaultProfile</span></span>
<span data-ttu-id="06b90-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06b90-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06b90-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06b90-121">-Description</span></span>
<span data-ttu-id="06b90-122">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="06b90-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="06b90-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="06b90-123">-DisplayName</span></span>
<span data-ttu-id="06b90-124">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="06b90-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="06b90-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="06b90-125">-Location</span></span>
<span data-ttu-id="06b90-126">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="06b90-126">The resource location.</span></span>

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

### <span data-ttu-id="06b90-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="06b90-127">-LockLevel</span></span>
<span data-ttu-id="06b90-128">Die Ebene der Sperre für die Definition einer verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="06b90-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="06b90-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="06b90-129">-MainTemplate</span></span>
<span data-ttu-id="06b90-130">Hauptvorlage für die verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="06b90-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="06b90-131">-Name</span><span class="sxs-lookup"><span data-stu-id="06b90-131">-Name</span></span>
<span data-ttu-id="06b90-132">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="06b90-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="06b90-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="06b90-133">-PackageFileUri</span></span>
<span data-ttu-id="06b90-134">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="06b90-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="06b90-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="06b90-135">-Pre</span></span>
<span data-ttu-id="06b90-136">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="06b90-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="06b90-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b90-137">-ResourceGroupName</span></span>
<span data-ttu-id="06b90-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06b90-138">The resource group name.</span></span>

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

### <span data-ttu-id="06b90-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="06b90-139">-Tag</span></span>
<span data-ttu-id="06b90-140">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="06b90-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="06b90-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06b90-141">-Confirm</span></span>
<span data-ttu-id="06b90-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06b90-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b90-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b90-143">-WhatIf</span></span>
<span data-ttu-id="06b90-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06b90-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b90-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06b90-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b90-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b90-146">CommonParameters</span></span>
<span data-ttu-id="06b90-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b90-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b90-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b90-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b90-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06b90-149">INPUTS</span></span>

### <span data-ttu-id="06b90-150">System. String</span><span class="sxs-lookup"><span data-stu-id="06b90-150">System.String</span></span>

### <span data-ttu-id="06b90-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="06b90-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="06b90-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="06b90-152">System.String[]</span></span>

### <span data-ttu-id="06b90-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06b90-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06b90-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06b90-154">OUTPUTS</span></span>

### <span data-ttu-id="06b90-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="06b90-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06b90-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="06b90-156">NOTES</span></span>

## <span data-ttu-id="06b90-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06b90-157">RELATED LINKS</span></span>
