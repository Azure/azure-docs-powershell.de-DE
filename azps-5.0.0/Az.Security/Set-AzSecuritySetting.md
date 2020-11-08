---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176396"
---
# <span data-ttu-id="71b3c-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="71b3c-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="71b3c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="71b3c-103">Aktualisieren einer Sicherheitseinstellung im Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="71b3c-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="71b3c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71b3c-104">SYNTAX</span></span>

### <span data-ttu-id="71b3c-105">GeneralScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="71b3c-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b3c-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="71b3c-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b3c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="71b3c-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b3c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71b3c-108">DESCRIPTION</span></span>
<span data-ttu-id="71b3c-109">Das Set-AzSecuritySetting-Cmdlet aktualisiert eine bestimmte Sicherheitseinstellung im Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="71b3c-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="71b3c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71b3c-110">EXAMPLES</span></span>

### <span data-ttu-id="71b3c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71b3c-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="71b3c-112">Aktualisiert eine MCAS-Datenexport Einstellung</span><span class="sxs-lookup"><span data-stu-id="71b3c-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="71b3c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="71b3c-113">PARAMETERS</span></span>

### <span data-ttu-id="71b3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b3c-114">-DefaultProfile</span></span>
<span data-ttu-id="71b3c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71b3c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71b3c-116">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="71b3c-116">-Enabled</span></span>
<span data-ttu-id="71b3c-117">Aktiviert die Einstellung.</span><span class="sxs-lookup"><span data-stu-id="71b3c-117">Enables the setting.</span></span>

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

### <span data-ttu-id="71b3c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71b3c-118">-InputObject</span></span>
<span data-ttu-id="71b3c-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="71b3c-119">Input Object.</span></span>

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

### <span data-ttu-id="71b3c-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="71b3c-120">-SettingKind</span></span>
<span data-ttu-id="71b3c-121">Art der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="71b3c-121">Setting kind.</span></span> <span data-ttu-id="71b3c-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="71b3c-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="71b3c-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="71b3c-123">-SettingName</span></span>
<span data-ttu-id="71b3c-124">Name der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="71b3c-124">Setting name.</span></span> <span data-ttu-id="71b3c-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="71b3c-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="71b3c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71b3c-126">-Confirm</span></span>
<span data-ttu-id="71b3c-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71b3c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b3c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b3c-128">-WhatIf</span></span>
<span data-ttu-id="71b3c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71b3c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b3c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71b3c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b3c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b3c-131">CommonParameters</span></span>
<span data-ttu-id="71b3c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b3c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b3c-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71b3c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b3c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71b3c-134">INPUTS</span></span>

### <span data-ttu-id="71b3c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="71b3c-135">System.String</span></span>
### <span data-ttu-id="71b3c-136">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="71b3c-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="71b3c-137">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="71b3c-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="71b3c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71b3c-138">System.Boolean</span></span>

## <span data-ttu-id="71b3c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71b3c-139">OUTPUTS</span></span>

### <span data-ttu-id="71b3c-140">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="71b3c-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="71b3c-141">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="71b3c-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="71b3c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="71b3c-142">NOTES</span></span>

## <span data-ttu-id="71b3c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71b3c-143">RELATED LINKS</span></span>
