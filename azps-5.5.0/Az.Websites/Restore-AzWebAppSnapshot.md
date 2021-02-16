---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149657"
---
# <span data-ttu-id="dedfa-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="dedfa-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="dedfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dedfa-102">SYNOPSIS</span></span>
<span data-ttu-id="dedfa-103">Stellt eine Web-App-Momentaufnahme wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dedfa-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="dedfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dedfa-104">SYNTAX</span></span>

### <span data-ttu-id="dedfa-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="dedfa-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dedfa-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="dedfa-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dedfa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dedfa-107">DESCRIPTION</span></span>
<span data-ttu-id="dedfa-108">Stellt eine Web-App-Momentaufnahme in der Web App wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dedfa-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="dedfa-109">Durch das Wiederherstellen einer Momentaufnahme werden alle Dateien in einer Web App mit den in der Momentaufnahme enthaltenen Dateien überschrieben.</span><span class="sxs-lookup"><span data-stu-id="dedfa-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="dedfa-110">Verwenden Sie zum Wiederherstellen von Einstellungen auch den Parameter des Switchparameters "RecoverConfiguration".</span><span class="sxs-lookup"><span data-stu-id="dedfa-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="dedfa-111">Eine Momentaufnahme aus einer Web App kann in jede andere Web App im selben Abonnement wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dedfa-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="dedfa-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dedfa-112">EXAMPLES</span></span>

### <span data-ttu-id="dedfa-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dedfa-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="dedfa-114">Ruft die neueste Momentaufnahme einer Web App namens "ContosoApp" mit dem Slot "Staging" in der Ressourcengruppe "Default-Web-WestUS" ab.</span><span class="sxs-lookup"><span data-stu-id="dedfa-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="dedfa-115">Stellt die Momentaufnahme auf dem "Wiederherstellen"-Platz der Web App wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dedfa-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="dedfa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dedfa-116">PARAMETERS</span></span>

### <span data-ttu-id="dedfa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dedfa-117">-AsJob</span></span>
<span data-ttu-id="dedfa-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dedfa-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dedfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedfa-119">-DefaultProfile</span></span>
<span data-ttu-id="dedfa-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dedfa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dedfa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dedfa-121">-Force</span></span>
<span data-ttu-id="dedfa-122">Ermöglicht das Überschreiben der ursprünglichen Web App ohne Anzeige einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="dedfa-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dedfa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dedfa-123">-InputObject</span></span>
<span data-ttu-id="dedfa-124">Die Azure Web App-Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="dedfa-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dedfa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dedfa-125">-Name</span></span>
<span data-ttu-id="dedfa-126">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="dedfa-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dedfa-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="dedfa-127">-RecoverConfiguration</span></span>
<span data-ttu-id="dedfa-128">Stellen Sie zusätzlich zu Dateien die Konfiguration der Web App wiederher.</span><span class="sxs-lookup"><span data-stu-id="dedfa-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dedfa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedfa-129">-ResourceGroupName</span></span>
<span data-ttu-id="dedfa-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dedfa-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dedfa-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="dedfa-131">-Slot</span></span>
<span data-ttu-id="dedfa-132">Der Name des Web-App-Slot.</span><span class="sxs-lookup"><span data-stu-id="dedfa-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dedfa-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="dedfa-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="dedfa-134">Wird verwendet, um eine Momentaufnahme einer Skalierungseinheit wiederhergestellt zu haben, die offline ist.</span><span class="sxs-lookup"><span data-stu-id="dedfa-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="dedfa-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dedfa-135">-WebApp</span></span>
<span data-ttu-id="dedfa-136">Web -App-Objekt</span><span class="sxs-lookup"><span data-stu-id="dedfa-136">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dedfa-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dedfa-137">-Confirm</span></span>
<span data-ttu-id="dedfa-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dedfa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dedfa-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dedfa-139">-WhatIf</span></span>
<span data-ttu-id="dedfa-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dedfa-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dedfa-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dedfa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dedfa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedfa-142">CommonParameters</span></span>
<span data-ttu-id="dedfa-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dedfa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedfa-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dedfa-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedfa-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dedfa-145">INPUTS</span></span>

### <span data-ttu-id="dedfa-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dedfa-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dedfa-147">System.String</span><span class="sxs-lookup"><span data-stu-id="dedfa-147">System.String</span></span>

### <span data-ttu-id="dedfa-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="dedfa-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="dedfa-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="dedfa-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="dedfa-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dedfa-150">OUTPUTS</span></span>

### <span data-ttu-id="dedfa-151">System.Void</span><span class="sxs-lookup"><span data-stu-id="dedfa-151">System.Void</span></span>

## <span data-ttu-id="dedfa-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dedfa-152">NOTES</span></span>

## <span data-ttu-id="dedfa-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dedfa-153">RELATED LINKS</span></span>
