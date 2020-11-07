---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4319a2637b2dbb008056a6b369ace539b889cd37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658586"
---
# <span data-ttu-id="59b20-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b20-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="59b20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59b20-102">SYNOPSIS</span></span>

## <span data-ttu-id="59b20-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="59b20-103">SYNTAX</span></span>

### <span data-ttu-id="59b20-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="59b20-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="59b20-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="59b20-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="59b20-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59b20-106">DESCRIPTION</span></span>
<span data-ttu-id="59b20-107">Das Cmdlet " **Edit-AzWebAppBackupConfiguration** " bearbeitet die aktuelle Backup-Konfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="59b20-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="59b20-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59b20-108">EXAMPLES</span></span>

## <span data-ttu-id="59b20-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="59b20-109">PARAMETERS</span></span>

### <span data-ttu-id="59b20-110">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="59b20-110">-Databases</span></span>
<span data-ttu-id="59b20-111">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="59b20-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b20-112">-DefaultProfile</span></span>
<span data-ttu-id="59b20-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59b20-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b20-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="59b20-114">-FrequencyInterval</span></span>
<span data-ttu-id="59b20-115">Häufigkeitsintervall</span><span class="sxs-lookup"><span data-stu-id="59b20-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b20-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="59b20-116">-FrequencyUnit</span></span>
<span data-ttu-id="59b20-117">Frequenzeinheit</span><span class="sxs-lookup"><span data-stu-id="59b20-117">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b20-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="59b20-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="59b20-119">Mindestens eine Sicherungs Option beibehalten</span><span class="sxs-lookup"><span data-stu-id="59b20-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b20-120">-Name</span><span class="sxs-lookup"><span data-stu-id="59b20-120">-Name</span></span>
<span data-ttu-id="59b20-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="59b20-121">WebApp Name</span></span>

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

### <span data-ttu-id="59b20-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b20-122">-ResourceGroupName</span></span>
<span data-ttu-id="59b20-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="59b20-123">Resource Group Name</span></span>

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

### <span data-ttu-id="59b20-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="59b20-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="59b20-125">Aufbewahrungszeitraum in Tagen</span><span class="sxs-lookup"><span data-stu-id="59b20-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b20-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="59b20-126">-Slot</span></span>
<span data-ttu-id="59b20-127">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="59b20-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="59b20-128">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="59b20-128">-StartTime</span></span>
<span data-ttu-id="59b20-129">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="59b20-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b20-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="59b20-130">-StorageAccountUrl</span></span>
<span data-ttu-id="59b20-131">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="59b20-131">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b20-132">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="59b20-132">-WebApp</span></span>
<span data-ttu-id="59b20-133">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="59b20-133">WebApp Object</span></span>

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

### <span data-ttu-id="59b20-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b20-134">CommonParameters</span></span>
<span data-ttu-id="59b20-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b20-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b20-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b20-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b20-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59b20-137">INPUTS</span></span>

### <span data-ttu-id="59b20-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="59b20-138">System.Int32</span></span>

### <span data-ttu-id="59b20-139">System. String</span><span class="sxs-lookup"><span data-stu-id="59b20-139">System.String</span></span>

### <span data-ttu-id="59b20-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="59b20-140">System.DateTime</span></span>

### <span data-ttu-id="59b20-141">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="59b20-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="59b20-142">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="59b20-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="59b20-143">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="59b20-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="59b20-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59b20-144">OUTPUTS</span></span>

### <span data-ttu-id="59b20-145">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b20-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="59b20-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="59b20-146">NOTES</span></span>

## <span data-ttu-id="59b20-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59b20-147">RELATED LINKS</span></span>

[<span data-ttu-id="59b20-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b20-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


