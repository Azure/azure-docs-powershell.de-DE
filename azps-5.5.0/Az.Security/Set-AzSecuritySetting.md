---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150788"
---
# <span data-ttu-id="040e5-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="040e5-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="040e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="040e5-102">SYNOPSIS</span></span>
<span data-ttu-id="040e5-103">Aktualisieren einer Sicherheitseinstellung im Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="040e5-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="040e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="040e5-104">SYNTAX</span></span>

### <span data-ttu-id="040e5-105">GeneralScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="040e5-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="040e5-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="040e5-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="040e5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="040e5-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="040e5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="040e5-108">DESCRIPTION</span></span>
<span data-ttu-id="040e5-109">Das Set-AzSecuritySetting aktualisiert eine bestimmte Sicherheitseinstellung im Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="040e5-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="040e5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="040e5-110">EXAMPLES</span></span>

### <span data-ttu-id="040e5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="040e5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="040e5-112">Aktualisiert eine MCAS-Datenexporteinstellung.</span><span class="sxs-lookup"><span data-stu-id="040e5-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="040e5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="040e5-113">PARAMETERS</span></span>

### <span data-ttu-id="040e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040e5-114">-DefaultProfile</span></span>
<span data-ttu-id="040e5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="040e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="040e5-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="040e5-116">-Enabled</span></span>
<span data-ttu-id="040e5-117">Aktiviert die Einstellung.</span><span class="sxs-lookup"><span data-stu-id="040e5-117">Enables the setting.</span></span>

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

### <span data-ttu-id="040e5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="040e5-118">-InputObject</span></span>
<span data-ttu-id="040e5-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="040e5-119">Input Object.</span></span>

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

### <span data-ttu-id="040e5-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="040e5-120">-SettingKind</span></span>
<span data-ttu-id="040e5-121">Festlegen der Art</span><span class="sxs-lookup"><span data-stu-id="040e5-121">Setting kind.</span></span> <span data-ttu-id="040e5-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="040e5-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="040e5-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="040e5-123">-SettingName</span></span>
<span data-ttu-id="040e5-124">Einstellungsname.</span><span class="sxs-lookup"><span data-stu-id="040e5-124">Setting name.</span></span> <span data-ttu-id="040e5-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="040e5-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="040e5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="040e5-126">-Confirm</span></span>
<span data-ttu-id="040e5-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="040e5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="040e5-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="040e5-128">-WhatIf</span></span>
<span data-ttu-id="040e5-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="040e5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="040e5-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="040e5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="040e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040e5-131">CommonParameters</span></span>
<span data-ttu-id="040e5-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="040e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040e5-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="040e5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040e5-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="040e5-134">INPUTS</span></span>

### <span data-ttu-id="040e5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="040e5-135">System.String</span></span>
### <span data-ttu-id="040e5-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="040e5-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="040e5-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="040e5-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="040e5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="040e5-138">System.Boolean</span></span>

## <span data-ttu-id="040e5-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="040e5-139">OUTPUTS</span></span>

### <span data-ttu-id="040e5-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="040e5-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="040e5-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="040e5-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="040e5-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="040e5-142">NOTES</span></span>

## <span data-ttu-id="040e5-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="040e5-143">RELATED LINKS</span></span>
