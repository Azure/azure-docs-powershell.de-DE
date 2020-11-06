---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481902"
---
# <span data-ttu-id="c3b26-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c3b26-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="c3b26-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3b26-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b26-103">Stellt einen Web-App-Schnappschuss wieder her.</span><span class="sxs-lookup"><span data-stu-id="c3b26-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3b26-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3b26-104">SYNTAX</span></span>

### <span data-ttu-id="c3b26-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c3b26-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3b26-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c3b26-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3b26-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3b26-107">DESCRIPTION</span></span>
<span data-ttu-id="c3b26-108">Stellt einen Web-App-Schnappschuss in der Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="c3b26-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="c3b26-109">Beim Wiederherstellen eines Snapshots werden alle Dateien in einer Web-App mit den im Snapshot enthaltenen Dateien überschrieben.</span><span class="sxs-lookup"><span data-stu-id="c3b26-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="c3b26-110">Wenn Sie die Einstellungen auch wiederherstellen möchten, verwenden Sie den Parameter RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3b26-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="c3b26-111">Ein Snapshot einer Web-App kann in einer beliebigen anderen Web-App im gleichen Abonnement wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c3b26-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="c3b26-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3b26-112">EXAMPLES</span></span>

### <span data-ttu-id="c3b26-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3b26-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="c3b26-114">Ruft den neuesten Snapshot einer Web-App mit dem Namen "ContosoApp" mit einem Slot mit dem Namen "Staging" in der Ressourcengruppe "Standard-Web-westus" ab.</span><span class="sxs-lookup"><span data-stu-id="c3b26-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="c3b26-115">Stellt den Snapshot im "Restore"-Steckplatz der Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="c3b26-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="c3b26-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3b26-116">PARAMETERS</span></span>

### <span data-ttu-id="c3b26-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3b26-117">-AsJob</span></span>
<span data-ttu-id="c3b26-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c3b26-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3b26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b26-119">-DefaultProfile</span></span>
<span data-ttu-id="c3b26-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3b26-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b26-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c3b26-121">-Force</span></span>
<span data-ttu-id="c3b26-122">Lässt die ursprüngliche Web-App überschrieben werden, ohne eine Warnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c3b26-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="c3b26-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3b26-123">-InputObject</span></span>
<span data-ttu-id="c3b26-124">Der Azure Web App-Snapshot</span><span class="sxs-lookup"><span data-stu-id="c3b26-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="c3b26-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c3b26-125">-Name</span></span>
<span data-ttu-id="c3b26-126">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="c3b26-126">The name of the web app.</span></span>

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

### <span data-ttu-id="c3b26-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3b26-127">-RecoverConfiguration</span></span>
<span data-ttu-id="c3b26-128">Wiederherstellen der Web-App-Konfiguration zusätzlich zu Dateien.</span><span class="sxs-lookup"><span data-stu-id="c3b26-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="c3b26-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b26-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3b26-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3b26-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3b26-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="c3b26-131">-Slot</span></span>
<span data-ttu-id="c3b26-132">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="c3b26-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="c3b26-133">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="c3b26-133">-WebApp</span></span>
<span data-ttu-id="c3b26-134">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="c3b26-134">The web app object</span></span>

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

### <span data-ttu-id="c3b26-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3b26-135">-Confirm</span></span>
<span data-ttu-id="c3b26-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3b26-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b26-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b26-137">-WhatIf</span></span>
<span data-ttu-id="c3b26-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3b26-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3b26-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3b26-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b26-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b26-140">CommonParameters</span></span>
<span data-ttu-id="c3b26-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b26-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b26-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3b26-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b26-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3b26-143">INPUTS</span></span>

### <span data-ttu-id="c3b26-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="c3b26-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c3b26-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c3b26-145">System.String</span></span>

### <span data-ttu-id="c3b26-146">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="c3b26-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c3b26-147">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="c3b26-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="c3b26-148">Microsoft. Azure. Commands. webapps. Cmdlets. backuprestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c3b26-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="c3b26-149">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3b26-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c3b26-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3b26-150">OUTPUTS</span></span>

### <span data-ttu-id="c3b26-151">System. void</span><span class="sxs-lookup"><span data-stu-id="c3b26-151">System.Void</span></span>

## <span data-ttu-id="c3b26-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3b26-152">NOTES</span></span>

## <span data-ttu-id="c3b26-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3b26-153">RELATED LINKS</span></span>
