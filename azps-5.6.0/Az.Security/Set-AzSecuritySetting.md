---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 5c7e9d80ffd9109cda1f13f74b1febb3b28e10ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945742"
---
# <span data-ttu-id="e1260-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="e1260-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="e1260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1260-102">SYNOPSIS</span></span>
<span data-ttu-id="e1260-103">Aktualisieren einer Sicherheitseinstellung in Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="e1260-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="e1260-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1260-104">SYNTAX</span></span>

### <span data-ttu-id="e1260-105">GeneralScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1260-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1260-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="e1260-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1260-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1260-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1260-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1260-108">DESCRIPTION</span></span>
<span data-ttu-id="e1260-109">Das Set-AzSecuritySetting-Cmdlet aktualisiert eine bestimmte Sicherheitseinstellung in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="e1260-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="e1260-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1260-110">EXAMPLES</span></span>

### <span data-ttu-id="e1260-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1260-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="e1260-112">Aktualisiert eine EINSTELLUNG für den MCAS-Datenexport</span><span class="sxs-lookup"><span data-stu-id="e1260-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="e1260-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e1260-113">PARAMETERS</span></span>

### <span data-ttu-id="e1260-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1260-114">-DefaultProfile</span></span>
<span data-ttu-id="e1260-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1260-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1260-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e1260-116">-Enabled</span></span>
<span data-ttu-id="e1260-117">Aktiviert die Einstellung.</span><span class="sxs-lookup"><span data-stu-id="e1260-117">Enables the setting.</span></span>

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

### <span data-ttu-id="e1260-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1260-118">-InputObject</span></span>
<span data-ttu-id="e1260-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="e1260-119">Input Object.</span></span>

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

### <span data-ttu-id="e1260-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="e1260-120">-SettingKind</span></span>
<span data-ttu-id="e1260-121">Festlegen der Art.</span><span class="sxs-lookup"><span data-stu-id="e1260-121">Setting kind.</span></span> <span data-ttu-id="e1260-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="e1260-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="e1260-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="e1260-123">-SettingName</span></span>
<span data-ttu-id="e1260-124">Einstellungsname.</span><span class="sxs-lookup"><span data-stu-id="e1260-124">Setting name.</span></span> <span data-ttu-id="e1260-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="e1260-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="e1260-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1260-126">-Confirm</span></span>
<span data-ttu-id="e1260-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1260-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1260-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1260-128">-WhatIf</span></span>
<span data-ttu-id="e1260-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1260-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1260-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1260-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1260-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1260-131">CommonParameters</span></span>
<span data-ttu-id="e1260-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1260-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1260-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1260-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1260-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1260-134">INPUTS</span></span>

### <span data-ttu-id="e1260-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e1260-135">System.String</span></span>
### <span data-ttu-id="e1260-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="e1260-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="e1260-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="e1260-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="e1260-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1260-138">System.Boolean</span></span>

## <span data-ttu-id="e1260-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1260-139">OUTPUTS</span></span>

### <span data-ttu-id="e1260-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="e1260-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="e1260-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="e1260-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="e1260-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e1260-142">NOTES</span></span>

## <span data-ttu-id="e1260-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e1260-143">RELATED LINKS</span></span>
