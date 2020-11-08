---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167139"
---
# <span data-ttu-id="9928e-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="9928e-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="9928e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9928e-102">SYNOPSIS</span></span>
<span data-ttu-id="9928e-103">Stellt einen Web-App-Schnappschuss wieder her.</span><span class="sxs-lookup"><span data-stu-id="9928e-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="9928e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9928e-104">SYNTAX</span></span>

### <span data-ttu-id="9928e-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9928e-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9928e-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9928e-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9928e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9928e-107">DESCRIPTION</span></span>
<span data-ttu-id="9928e-108">Stellt einen Web-App-Schnappschuss in der Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="9928e-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="9928e-109">Beim Wiederherstellen eines Snapshots werden alle Dateien in einer Web-App mit den im Snapshot enthaltenen Dateien überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9928e-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="9928e-110">Wenn Sie die Einstellungen auch wiederherstellen möchten, verwenden Sie den Parameter RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9928e-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="9928e-111">Ein Snapshot einer Web-App kann in einer beliebigen anderen Web-App im gleichen Abonnement wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9928e-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="9928e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9928e-112">EXAMPLES</span></span>

### <span data-ttu-id="9928e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9928e-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="9928e-114">Ruft den neuesten Snapshot einer Web-App mit dem Namen "ContosoApp" mit einem Slot mit dem Namen "Staging" in der Ressourcengruppe "Standard-Web-westus" ab.</span><span class="sxs-lookup"><span data-stu-id="9928e-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="9928e-115">Stellt den Snapshot im "Restore"-Steckplatz der Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="9928e-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="9928e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9928e-116">PARAMETERS</span></span>

### <span data-ttu-id="9928e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9928e-117">-AsJob</span></span>
<span data-ttu-id="9928e-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9928e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9928e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9928e-119">-DefaultProfile</span></span>
<span data-ttu-id="9928e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9928e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9928e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9928e-121">-Force</span></span>
<span data-ttu-id="9928e-122">Lässt die ursprüngliche Web-App überschrieben werden, ohne eine Warnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9928e-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="9928e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9928e-123">-InputObject</span></span>
<span data-ttu-id="9928e-124">Der Azure Web App-Snapshot</span><span class="sxs-lookup"><span data-stu-id="9928e-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="9928e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9928e-125">-Name</span></span>
<span data-ttu-id="9928e-126">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="9928e-126">The name of the web app.</span></span>

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

### <span data-ttu-id="9928e-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="9928e-127">-RecoverConfiguration</span></span>
<span data-ttu-id="9928e-128">Wiederherstellen der Web-App-Konfiguration zusätzlich zu Dateien.</span><span class="sxs-lookup"><span data-stu-id="9928e-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="9928e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9928e-129">-ResourceGroupName</span></span>
<span data-ttu-id="9928e-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9928e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9928e-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="9928e-131">-Slot</span></span>
<span data-ttu-id="9928e-132">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="9928e-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="9928e-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="9928e-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="9928e-134">Dient zum Wiederherstellen eines Snapshots aus einer Offline skalierten Einheit.</span><span class="sxs-lookup"><span data-stu-id="9928e-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="9928e-135">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9928e-135">-WebApp</span></span>
<span data-ttu-id="9928e-136">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="9928e-136">The web app object</span></span>

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

### <span data-ttu-id="9928e-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9928e-137">-Confirm</span></span>
<span data-ttu-id="9928e-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9928e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9928e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9928e-139">-WhatIf</span></span>
<span data-ttu-id="9928e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9928e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9928e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9928e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9928e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9928e-142">CommonParameters</span></span>
<span data-ttu-id="9928e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9928e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9928e-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9928e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9928e-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9928e-145">INPUTS</span></span>

### <span data-ttu-id="9928e-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="9928e-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9928e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9928e-147">System.String</span></span>

### <span data-ttu-id="9928e-148">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9928e-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="9928e-149">Microsoft. Azure. Commands. webapps. Cmdlets. backuprestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="9928e-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="9928e-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9928e-150">OUTPUTS</span></span>

### <span data-ttu-id="9928e-151">System. void</span><span class="sxs-lookup"><span data-stu-id="9928e-151">System.Void</span></span>

## <span data-ttu-id="9928e-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="9928e-152">NOTES</span></span>

## <span data-ttu-id="9928e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9928e-153">RELATED LINKS</span></span>
