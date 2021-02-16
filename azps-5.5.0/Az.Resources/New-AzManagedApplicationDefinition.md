---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153636"
---
# <span data-ttu-id="60921-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="60921-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="60921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60921-102">SYNOPSIS</span></span>
<span data-ttu-id="60921-103">Erstellt eine Definition für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="60921-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="60921-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60921-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60921-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60921-105">DESCRIPTION</span></span>
<span data-ttu-id="60921-106">Das **Cmdlet "New-AzManagedApplicationDefinition"** erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="60921-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="60921-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60921-107">EXAMPLES</span></span>

### <span data-ttu-id="60921-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60921-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="60921-109">Mit diesem Befehl wird eine Definition für verwaltete Anwendungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="60921-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="60921-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60921-110">PARAMETERS</span></span>

### <span data-ttu-id="60921-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="60921-111">-ApiVersion</span></span>
<span data-ttu-id="60921-112">Gibt im festgelegten Satz die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="60921-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="60921-113">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="60921-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="60921-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="60921-114">-Authorization</span></span>
<span data-ttu-id="60921-115">Die Autorisierung für verwaltete Anwendungsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="60921-115">The managed application definition authorization.</span></span>
<span data-ttu-id="60921-116">Durch Kommas getrennte Autorisierungspaare in einem Format \<principalId\> von:\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="60921-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="60921-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="60921-117">-CreateUiDefinition</span></span>
<span data-ttu-id="60921-118">Definition der verwalteten Anwendung zum Erstellen einer Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="60921-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="60921-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60921-119">-DefaultProfile</span></span>
<span data-ttu-id="60921-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60921-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60921-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60921-121">-Description</span></span>
<span data-ttu-id="60921-122">Beschreibung der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="60921-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="60921-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="60921-123">-DisplayName</span></span>
<span data-ttu-id="60921-124">Anzeigename der verwalteten Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="60921-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="60921-125">-Location</span><span class="sxs-lookup"><span data-stu-id="60921-125">-Location</span></span>
<span data-ttu-id="60921-126">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="60921-126">The resource location.</span></span>

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

### <span data-ttu-id="60921-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="60921-127">-LockLevel</span></span>
<span data-ttu-id="60921-128">Die Ebene der Sperre für die Definition verwalteter Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="60921-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="60921-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="60921-129">-MainTemplate</span></span>
<span data-ttu-id="60921-130">Die Hauptvorlage für verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="60921-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="60921-131">-Name</span><span class="sxs-lookup"><span data-stu-id="60921-131">-Name</span></span>
<span data-ttu-id="60921-132">Der Name der verwalteten Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="60921-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="60921-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="60921-133">-PackageFileUri</span></span>
<span data-ttu-id="60921-134">Der URI für verwaltete Anwendungsdefinitionspaketdateien.</span><span class="sxs-lookup"><span data-stu-id="60921-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="60921-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="60921-135">-Pre</span></span>
<span data-ttu-id="60921-136">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60921-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="60921-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60921-137">-ResourceGroupName</span></span>
<span data-ttu-id="60921-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60921-138">The resource group name.</span></span>

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

### <span data-ttu-id="60921-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="60921-139">-Tag</span></span>
<span data-ttu-id="60921-140">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="60921-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="60921-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60921-141">-Confirm</span></span>
<span data-ttu-id="60921-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60921-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60921-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="60921-143">-WhatIf</span></span>
<span data-ttu-id="60921-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60921-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60921-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60921-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60921-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60921-146">CommonParameters</span></span>
<span data-ttu-id="60921-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60921-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60921-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60921-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60921-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60921-149">INPUTS</span></span>

### <span data-ttu-id="60921-150">System.String</span><span class="sxs-lookup"><span data-stu-id="60921-150">System.String</span></span>

### <span data-ttu-id="60921-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="60921-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="60921-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="60921-152">System.String[]</span></span>

### <span data-ttu-id="60921-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="60921-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="60921-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60921-154">OUTPUTS</span></span>

### <span data-ttu-id="60921-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="60921-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="60921-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60921-156">NOTES</span></span>

## <span data-ttu-id="60921-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60921-157">RELATED LINKS</span></span>
