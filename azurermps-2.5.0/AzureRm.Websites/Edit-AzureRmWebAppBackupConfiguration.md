---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 9a90e56909de016bb388be1a43f5b41c8e47e9e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848628"
---
# <span data-ttu-id="0f864-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f864-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="0f864-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f864-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f864-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f864-103">SYNTAX</span></span>

### <span data-ttu-id="0f864-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0f864-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="0f864-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0f864-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="0f864-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f864-106">DESCRIPTION</span></span>
<span data-ttu-id="0f864-107">Das Cmdlet " **Edit-AzureRmWebAppBackupConfiguration** " bearbeitet die aktuelle Backup-Konfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0f864-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="0f864-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f864-108">EXAMPLES</span></span>

## <span data-ttu-id="0f864-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f864-109">PARAMETERS</span></span>

### <span data-ttu-id="0f864-110">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="0f864-110">-Databases</span></span>
<span data-ttu-id="0f864-111">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="0f864-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f864-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f864-112">-DefaultProfile</span></span>
<span data-ttu-id="0f864-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f864-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f864-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="0f864-114">-FrequencyInterval</span></span>
<span data-ttu-id="0f864-115">Häufigkeitsintervall</span><span class="sxs-lookup"><span data-stu-id="0f864-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f864-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="0f864-116">-FrequencyUnit</span></span>
<span data-ttu-id="0f864-117">Frequenzeinheit</span><span class="sxs-lookup"><span data-stu-id="0f864-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f864-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="0f864-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="0f864-119">Mindestens eine Sicherungs Option beibehalten</span><span class="sxs-lookup"><span data-stu-id="0f864-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f864-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0f864-120">-Name</span></span>
<span data-ttu-id="0f864-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0f864-121">WebApp Name</span></span>

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

### <span data-ttu-id="0f864-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f864-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f864-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0f864-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0f864-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="0f864-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="0f864-125">Aufbewahrungszeitraum in Tagen</span><span class="sxs-lookup"><span data-stu-id="0f864-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f864-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="0f864-126">-Slot</span></span>
<span data-ttu-id="0f864-127">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="0f864-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0f864-128">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="0f864-128">-StartTime</span></span>
<span data-ttu-id="0f864-129">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="0f864-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f864-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="0f864-130">-StorageAccountUrl</span></span>
<span data-ttu-id="0f864-131">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="0f864-131">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f864-132">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0f864-132">-WebApp</span></span>
<span data-ttu-id="0f864-133">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="0f864-133">WebApp Object</span></span>

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

### <span data-ttu-id="0f864-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f864-134">CommonParameters</span></span>
<span data-ttu-id="0f864-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f864-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f864-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f864-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f864-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f864-137">INPUTS</span></span>

### <span data-ttu-id="0f864-138">Website</span><span class="sxs-lookup"><span data-stu-id="0f864-138">Site</span></span>
<span data-ttu-id="0f864-139">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f864-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0f864-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f864-140">OUTPUTS</span></span>

### <span data-ttu-id="0f864-141">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f864-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="0f864-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f864-142">NOTES</span></span>

## <span data-ttu-id="0f864-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f864-143">RELATED LINKS</span></span>

[<span data-ttu-id="0f864-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f864-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


