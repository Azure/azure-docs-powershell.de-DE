---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471994"
---
# <span data-ttu-id="deaa6-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="deaa6-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="deaa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="deaa6-103">Aktualisieren einer Sicherheitseinstellung im Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="deaa6-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="deaa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deaa6-104">SYNTAX</span></span>

### <span data-ttu-id="deaa6-105">GeneralScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="deaa6-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deaa6-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="deaa6-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deaa6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="deaa6-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deaa6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="deaa6-108">DESCRIPTION</span></span>
<span data-ttu-id="deaa6-109">Das Set-AzSecuritySetting aktualisiert eine bestimmte Sicherheitseinstellung im Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="deaa6-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="deaa6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="deaa6-110">EXAMPLES</span></span>

### <span data-ttu-id="deaa6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="deaa6-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="deaa6-112">Aktualisiert eine MCAS-Datenexporteinstellung.</span><span class="sxs-lookup"><span data-stu-id="deaa6-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="deaa6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deaa6-113">PARAMETERS</span></span>

### <span data-ttu-id="deaa6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deaa6-114">-DefaultProfile</span></span>
<span data-ttu-id="deaa6-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="deaa6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deaa6-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="deaa6-116">-Enabled</span></span>
<span data-ttu-id="deaa6-117">Aktiviert die Einstellung.</span><span class="sxs-lookup"><span data-stu-id="deaa6-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deaa6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deaa6-118">-InputObject</span></span>
<span data-ttu-id="deaa6-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="deaa6-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deaa6-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="deaa6-120">-SettingKind</span></span>
<span data-ttu-id="deaa6-121">Festlegen der Art</span><span class="sxs-lookup"><span data-stu-id="deaa6-121">Setting kind.</span></span> <span data-ttu-id="deaa6-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="deaa6-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deaa6-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="deaa6-123">-SettingName</span></span>
<span data-ttu-id="deaa6-124">Einstellungsname.</span><span class="sxs-lookup"><span data-stu-id="deaa6-124">Setting name.</span></span> <span data-ttu-id="deaa6-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="deaa6-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deaa6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="deaa6-126">-Confirm</span></span>
<span data-ttu-id="deaa6-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="deaa6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deaa6-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="deaa6-128">-WhatIf</span></span>
<span data-ttu-id="deaa6-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="deaa6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deaa6-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="deaa6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deaa6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deaa6-131">CommonParameters</span></span>
<span data-ttu-id="deaa6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deaa6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deaa6-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="deaa6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deaa6-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="deaa6-134">INPUTS</span></span>

### <span data-ttu-id="deaa6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="deaa6-135">System.String</span></span>
### <span data-ttu-id="deaa6-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="deaa6-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="deaa6-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="deaa6-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="deaa6-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="deaa6-138">System.Boolean</span></span>

## <span data-ttu-id="deaa6-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="deaa6-139">OUTPUTS</span></span>

### <span data-ttu-id="deaa6-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="deaa6-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="deaa6-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="deaa6-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="deaa6-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="deaa6-142">NOTES</span></span>

## <span data-ttu-id="deaa6-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="deaa6-143">RELATED LINKS</span></span>
