---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842819"
---
# <span data-ttu-id="2bfc9-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bfc9-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="2bfc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bfc9-102">SYNOPSIS</span></span>

## <span data-ttu-id="2bfc9-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bfc9-103">SYNTAX</span></span>

### <span data-ttu-id="2bfc9-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2bfc9-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="2bfc9-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2bfc9-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="2bfc9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bfc9-106">DESCRIPTION</span></span>
<span data-ttu-id="2bfc9-107">Das Cmdlet " **Edit-AzWebAppBackupConfiguration** " bearbeitet die aktuelle Backup-Konfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2bfc9-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="2bfc9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bfc9-108">EXAMPLES</span></span>

## <span data-ttu-id="2bfc9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bfc9-109">PARAMETERS</span></span>

### <span data-ttu-id="2bfc9-110">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="2bfc9-110">-Databases</span></span>
<span data-ttu-id="2bfc9-111">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="2bfc9-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="2bfc9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bfc9-112">-DefaultProfile</span></span>
<span data-ttu-id="2bfc9-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bfc9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfc9-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="2bfc9-114">-FrequencyInterval</span></span>
<span data-ttu-id="2bfc9-115">Häufigkeitsintervall</span><span class="sxs-lookup"><span data-stu-id="2bfc9-115">Frequency Interval</span></span>

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

### <span data-ttu-id="2bfc9-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="2bfc9-116">-FrequencyUnit</span></span>
<span data-ttu-id="2bfc9-117">Frequenzeinheit</span><span class="sxs-lookup"><span data-stu-id="2bfc9-117">Frequency Unit</span></span>

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

### <span data-ttu-id="2bfc9-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="2bfc9-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="2bfc9-119">Mindestens eine Sicherungs Option beibehalten</span><span class="sxs-lookup"><span data-stu-id="2bfc9-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="2bfc9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2bfc9-120">-Name</span></span>
<span data-ttu-id="2bfc9-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="2bfc9-121">WebApp Name</span></span>

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

### <span data-ttu-id="2bfc9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bfc9-122">-ResourceGroupName</span></span>
<span data-ttu-id="2bfc9-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2bfc9-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2bfc9-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="2bfc9-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="2bfc9-125">Aufbewahrungszeitraum in Tagen</span><span class="sxs-lookup"><span data-stu-id="2bfc9-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="2bfc9-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="2bfc9-126">-Slot</span></span>
<span data-ttu-id="2bfc9-127">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="2bfc9-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2bfc9-128">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="2bfc9-128">-StartTime</span></span>
<span data-ttu-id="2bfc9-129">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="2bfc9-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="2bfc9-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="2bfc9-130">-StorageAccountUrl</span></span>
<span data-ttu-id="2bfc9-131">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="2bfc9-131">Storage Account Url</span></span>

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

### <span data-ttu-id="2bfc9-132">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="2bfc9-132">-WebApp</span></span>
<span data-ttu-id="2bfc9-133">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="2bfc9-133">WebApp Object</span></span>

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

### <span data-ttu-id="2bfc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfc9-134">CommonParameters</span></span>
<span data-ttu-id="2bfc9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bfc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfc9-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfc9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfc9-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bfc9-137">INPUTS</span></span>

### <span data-ttu-id="2bfc9-138">Website</span><span class="sxs-lookup"><span data-stu-id="2bfc9-138">Site</span></span>
<span data-ttu-id="2bfc9-139">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2bfc9-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2bfc9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bfc9-140">OUTPUTS</span></span>

### <span data-ttu-id="2bfc9-141">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bfc9-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="2bfc9-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bfc9-142">NOTES</span></span>

## <span data-ttu-id="2bfc9-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bfc9-143">RELATED LINKS</span></span>

[<span data-ttu-id="2bfc9-144">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bfc9-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


