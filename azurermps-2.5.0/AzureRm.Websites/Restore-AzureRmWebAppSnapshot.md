---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 0719210cae275dc7e250e7fd14e622c51014d7c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850200"
---
# <span data-ttu-id="c8261-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="c8261-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="c8261-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8261-102">SYNOPSIS</span></span>
<span data-ttu-id="c8261-103">Stellt einen Web-App-Schnappschuss wieder her.</span><span class="sxs-lookup"><span data-stu-id="c8261-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8261-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8261-104">SYNTAX</span></span>

### <span data-ttu-id="c8261-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c8261-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8261-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c8261-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8261-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8261-107">DESCRIPTION</span></span>
<span data-ttu-id="c8261-108">Stellt einen Web-App-Schnappschuss in der Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="c8261-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="c8261-109">Beim Wiederherstellen eines Snapshots werden alle Dateien in einer Web-App mit den im Snapshot enthaltenen Dateien überschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8261-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="c8261-110">Wenn Sie die Einstellungen auch wiederherstellen möchten, verwenden Sie den Parameter RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c8261-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="c8261-111">Ein Snapshot einer Web-App kann in einer beliebigen anderen Web-App im gleichen Abonnement wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8261-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="c8261-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8261-112">EXAMPLES</span></span>

### <span data-ttu-id="c8261-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c8261-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="c8261-114">Ruft den neuesten Snapshot einer Web-App mit dem Namen "ContosoApp" mit einem Slot mit dem Namen "Staging" in der Ressourcengruppe "Standard-Web-westus" ab.</span><span class="sxs-lookup"><span data-stu-id="c8261-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="c8261-115">Stellt den Snapshot im "Restore"-Steckplatz der Web-App wieder her.</span><span class="sxs-lookup"><span data-stu-id="c8261-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="c8261-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8261-116">PARAMETERS</span></span>

### <span data-ttu-id="c8261-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8261-117">-AsJob</span></span>
<span data-ttu-id="c8261-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c8261-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8261-119">-DefaultProfile</span></span>
<span data-ttu-id="c8261-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8261-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c8261-121">-Force</span></span>
<span data-ttu-id="c8261-122">Lässt die ursprüngliche Web-App überschrieben werden, ohne eine Warnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8261-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8261-123">-InputObject</span></span>
<span data-ttu-id="c8261-124">Der Azure Web App-Snapshot</span><span class="sxs-lookup"><span data-stu-id="c8261-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c8261-125">-Name</span></span>
<span data-ttu-id="c8261-126">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="c8261-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8261-127">-RecoverConfiguration</span></span>
<span data-ttu-id="c8261-128">Wiederherstellen der Web-App-Konfiguration zusätzlich zu Dateien.</span><span class="sxs-lookup"><span data-stu-id="c8261-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8261-129">-ResourceGroupName</span></span>
<span data-ttu-id="c8261-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c8261-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="c8261-131">-Slot</span></span>
<span data-ttu-id="c8261-132">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="c8261-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-133">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="c8261-133">-WebApp</span></span>
<span data-ttu-id="c8261-134">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="c8261-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8261-135">-Confirm</span></span>
<span data-ttu-id="c8261-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8261-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8261-137">-WhatIf</span></span>
<span data-ttu-id="c8261-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8261-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8261-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8261-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8261-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8261-140">CommonParameters</span></span>
<span data-ttu-id="c8261-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8261-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8261-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8261-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8261-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8261-143">INPUTS</span></span>

### <span data-ttu-id="c8261-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="c8261-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="c8261-145">Microsoft. Azure. Management. Websites. Models. Site System. String Microsoft. Azure. Commands. webapps. Cmdlets. backuprestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c8261-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="c8261-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8261-146">OUTPUTS</span></span>

### <span data-ttu-id="c8261-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="c8261-147">System.Object</span></span>

## <span data-ttu-id="c8261-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8261-148">NOTES</span></span>

## <span data-ttu-id="c8261-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8261-149">RELATED LINKS</span></span>

