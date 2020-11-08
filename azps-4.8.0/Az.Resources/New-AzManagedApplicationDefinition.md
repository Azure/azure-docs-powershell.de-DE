---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007864"
---
# <span data-ttu-id="3df17-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="3df17-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="3df17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3df17-102">SYNOPSIS</span></span>
<span data-ttu-id="3df17-103">Erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="3df17-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="3df17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3df17-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3df17-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3df17-105">DESCRIPTION</span></span>
<span data-ttu-id="3df17-106">Das Cmdlet **New-AzManagedApplicationDefinition** erstellt eine verwaltete Anwendungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="3df17-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="3df17-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3df17-107">EXAMPLES</span></span>

### <span data-ttu-id="3df17-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3df17-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="3df17-109">Mit diesem Befehl wird eine verwaltete Anwendungsdefinition erstellt</span><span class="sxs-lookup"><span data-stu-id="3df17-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="3df17-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3df17-110">PARAMETERS</span></span>

### <span data-ttu-id="3df17-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3df17-111">-ApiVersion</span></span>
<span data-ttu-id="3df17-112">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3df17-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3df17-113">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3df17-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3df17-114">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="3df17-114">-Authorization</span></span>
<span data-ttu-id="3df17-115">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3df17-115">The managed application definition authorization.</span></span>
<span data-ttu-id="3df17-116">Durch trennzeichengetrennte Autorisierungs Paare im Format \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="3df17-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="3df17-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="3df17-117">-CreateUiDefinition</span></span>
<span data-ttu-id="3df17-118">Definition der verwalteten Anwendung erstellen einer UI-Definition</span><span class="sxs-lookup"><span data-stu-id="3df17-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="3df17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df17-119">-DefaultProfile</span></span>
<span data-ttu-id="3df17-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3df17-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df17-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3df17-121">-Description</span></span>
<span data-ttu-id="3df17-122">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="3df17-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="3df17-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3df17-123">-DisplayName</span></span>
<span data-ttu-id="3df17-124">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="3df17-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="3df17-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="3df17-125">-Location</span></span>
<span data-ttu-id="3df17-126">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3df17-126">The resource location.</span></span>

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

### <span data-ttu-id="3df17-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="3df17-127">-LockLevel</span></span>
<span data-ttu-id="3df17-128">Die Ebene der Sperre für die Definition einer verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3df17-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="3df17-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="3df17-129">-MainTemplate</span></span>
<span data-ttu-id="3df17-130">Hauptvorlage für die verwaltete Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="3df17-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="3df17-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3df17-131">-Name</span></span>
<span data-ttu-id="3df17-132">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3df17-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="3df17-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="3df17-133">-PackageFileUri</span></span>
<span data-ttu-id="3df17-134">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="3df17-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="3df17-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="3df17-135">-Pre</span></span>
<span data-ttu-id="3df17-136">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="3df17-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3df17-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df17-137">-ResourceGroupName</span></span>
<span data-ttu-id="3df17-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3df17-138">The resource group name.</span></span>

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

### <span data-ttu-id="3df17-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="3df17-139">-Tag</span></span>
<span data-ttu-id="3df17-140">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="3df17-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3df17-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3df17-141">-Confirm</span></span>
<span data-ttu-id="3df17-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3df17-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df17-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df17-143">-WhatIf</span></span>
<span data-ttu-id="3df17-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3df17-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df17-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3df17-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df17-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df17-146">CommonParameters</span></span>
<span data-ttu-id="3df17-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df17-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df17-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3df17-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df17-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3df17-149">INPUTS</span></span>

### <span data-ttu-id="3df17-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3df17-150">System.String</span></span>

### <span data-ttu-id="3df17-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="3df17-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="3df17-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="3df17-152">System.String[]</span></span>

### <span data-ttu-id="3df17-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3df17-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3df17-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3df17-154">OUTPUTS</span></span>

### <span data-ttu-id="3df17-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3df17-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3df17-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="3df17-156">NOTES</span></span>

## <span data-ttu-id="3df17-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3df17-157">RELATED LINKS</span></span>
