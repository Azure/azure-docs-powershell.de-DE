---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 490f7b4a0cb723d02deb1d18e8a2ddfb993e7f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996379"
---
# <span data-ttu-id="7b298-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b298-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7b298-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b298-102">SYNOPSIS</span></span>

## <span data-ttu-id="7b298-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b298-103">SYNTAX</span></span>

### <span data-ttu-id="7b298-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7b298-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="7b298-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7b298-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="7b298-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b298-106">DESCRIPTION</span></span>
<span data-ttu-id="7b298-107">Das Cmdlet " **Edit-AzWebAppBackupConfiguration** " bearbeitet die aktuelle Backup-Konfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7b298-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="7b298-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b298-108">EXAMPLES</span></span>

## <span data-ttu-id="7b298-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b298-109">PARAMETERS</span></span>

### <span data-ttu-id="7b298-110">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="7b298-110">-Databases</span></span>
<span data-ttu-id="7b298-111">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="7b298-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="7b298-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b298-112">-DefaultProfile</span></span>
<span data-ttu-id="7b298-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b298-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b298-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="7b298-114">-FrequencyInterval</span></span>
<span data-ttu-id="7b298-115">Häufigkeitsintervall</span><span class="sxs-lookup"><span data-stu-id="7b298-115">Frequency Interval</span></span>

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

### <span data-ttu-id="7b298-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="7b298-116">-FrequencyUnit</span></span>
<span data-ttu-id="7b298-117">Frequenzeinheit</span><span class="sxs-lookup"><span data-stu-id="7b298-117">Frequency Unit</span></span>

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

### <span data-ttu-id="7b298-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="7b298-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="7b298-119">Mindestens eine Sicherungs Option beibehalten</span><span class="sxs-lookup"><span data-stu-id="7b298-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="7b298-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7b298-120">-Name</span></span>
<span data-ttu-id="7b298-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7b298-121">WebApp Name</span></span>

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

### <span data-ttu-id="7b298-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b298-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b298-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7b298-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7b298-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="7b298-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="7b298-125">Aufbewahrungszeitraum in Tagen</span><span class="sxs-lookup"><span data-stu-id="7b298-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="7b298-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="7b298-126">-Slot</span></span>
<span data-ttu-id="7b298-127">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="7b298-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7b298-128">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="7b298-128">-StartTime</span></span>
<span data-ttu-id="7b298-129">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="7b298-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="7b298-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="7b298-130">-StorageAccountUrl</span></span>
<span data-ttu-id="7b298-131">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="7b298-131">Storage Account Url</span></span>

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

### <span data-ttu-id="7b298-132">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="7b298-132">-WebApp</span></span>
<span data-ttu-id="7b298-133">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="7b298-133">WebApp Object</span></span>

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

### <span data-ttu-id="7b298-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b298-134">CommonParameters</span></span>
<span data-ttu-id="7b298-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b298-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b298-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b298-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b298-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b298-137">INPUTS</span></span>

### <span data-ttu-id="7b298-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7b298-138">System.Int32</span></span>

### <span data-ttu-id="7b298-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7b298-139">System.String</span></span>

### <span data-ttu-id="7b298-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="7b298-140">System.DateTime</span></span>

### <span data-ttu-id="7b298-141">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7b298-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7b298-142">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="7b298-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="7b298-143">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="7b298-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="7b298-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b298-144">OUTPUTS</span></span>

### <span data-ttu-id="7b298-145">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b298-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7b298-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b298-146">NOTES</span></span>

## <span data-ttu-id="7b298-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b298-147">RELATED LINKS</span></span>

[<span data-ttu-id="7b298-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b298-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


