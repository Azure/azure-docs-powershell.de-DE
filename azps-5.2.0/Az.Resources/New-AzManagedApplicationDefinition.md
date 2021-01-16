---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358026"
---
# <span data-ttu-id="6a706-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="6a706-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="6a706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a706-102">SYNOPSIS</span></span>
<span data-ttu-id="6a706-103">Erstellt eine Definition für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6a706-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="6a706-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a706-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a706-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a706-105">DESCRIPTION</span></span>
<span data-ttu-id="6a706-106">Das **Cmdlet "New-AzManagedApplicationDefinition"** erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="6a706-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="6a706-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a706-107">EXAMPLES</span></span>

### <span data-ttu-id="6a706-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a706-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="6a706-109">Mit diesem Befehl wird eine Definition verwalteter Anwendungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a706-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="6a706-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a706-110">PARAMETERS</span></span>

### <span data-ttu-id="6a706-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6a706-111">-ApiVersion</span></span>
<span data-ttu-id="6a706-112">Wenn dies festgelegt ist, wird die Version der zu verwendenden Ressourcenanbieter-API angegeben.</span><span class="sxs-lookup"><span data-stu-id="6a706-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6a706-113">Wenn keine Angabe erfolgt, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6a706-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6a706-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="6a706-114">-Authorization</span></span>
<span data-ttu-id="6a706-115">Die Autorisierung für verwaltete Anwendungsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6a706-115">The managed application definition authorization.</span></span>
<span data-ttu-id="6a706-116">Durch Kommas getrennte Autorisierungspaare in einem Format \<principalId\> von:\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="6a706-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="6a706-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="6a706-117">-CreateUiDefinition</span></span>
<span data-ttu-id="6a706-118">Definition der verwalteten Anwendung zum Erstellen einer Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="6a706-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="6a706-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a706-119">-DefaultProfile</span></span>
<span data-ttu-id="6a706-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a706-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a706-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a706-121">-Description</span></span>
<span data-ttu-id="6a706-122">Beschreibung der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="6a706-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="6a706-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6a706-123">-DisplayName</span></span>
<span data-ttu-id="6a706-124">Anzeigename der verwalteten Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="6a706-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="6a706-125">-Location</span><span class="sxs-lookup"><span data-stu-id="6a706-125">-Location</span></span>
<span data-ttu-id="6a706-126">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="6a706-126">The resource location.</span></span>

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

### <span data-ttu-id="6a706-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="6a706-127">-LockLevel</span></span>
<span data-ttu-id="6a706-128">Die Ebene der Sperre für die Definition verwalteter Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6a706-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="6a706-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="6a706-129">-MainTemplate</span></span>
<span data-ttu-id="6a706-130">Die Hauptvorlage für verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="6a706-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="6a706-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6a706-131">-Name</span></span>
<span data-ttu-id="6a706-132">Der Name der verwalteten Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="6a706-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="6a706-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="6a706-133">-PackageFileUri</span></span>
<span data-ttu-id="6a706-134">Der URI für verwaltete Anwendungsdefinitionspaketdateien.</span><span class="sxs-lookup"><span data-stu-id="6a706-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="6a706-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6a706-135">-Pre</span></span>
<span data-ttu-id="6a706-136">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a706-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6a706-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a706-137">-ResourceGroupName</span></span>
<span data-ttu-id="6a706-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a706-138">The resource group name.</span></span>

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

### <span data-ttu-id="6a706-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a706-139">-Tag</span></span>
<span data-ttu-id="6a706-140">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="6a706-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6a706-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a706-141">-Confirm</span></span>
<span data-ttu-id="6a706-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a706-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a706-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6a706-143">-WhatIf</span></span>
<span data-ttu-id="6a706-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a706-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a706-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a706-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a706-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a706-146">CommonParameters</span></span>
<span data-ttu-id="6a706-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a706-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a706-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a706-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a706-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a706-149">INPUTS</span></span>

### <span data-ttu-id="6a706-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6a706-150">System.String</span></span>

### <span data-ttu-id="6a706-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="6a706-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="6a706-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6a706-152">System.String[]</span></span>

### <span data-ttu-id="6a706-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a706-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6a706-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a706-154">OUTPUTS</span></span>

### <span data-ttu-id="6a706-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6a706-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6a706-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a706-156">NOTES</span></span>

## <span data-ttu-id="6a706-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a706-157">RELATED LINKS</span></span>
