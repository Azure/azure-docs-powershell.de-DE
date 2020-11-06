---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481402"
---
# <span data-ttu-id="ce176-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce176-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ce176-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce176-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce176-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce176-103">SYNTAX</span></span>

### <span data-ttu-id="ce176-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ce176-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ce176-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ce176-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ce176-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce176-106">DESCRIPTION</span></span>
<span data-ttu-id="ce176-107">Das Cmdlet " **Edit-AzureRmWebAppBackupConfiguration** " bearbeitet die aktuelle Backup-Konfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ce176-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="ce176-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce176-108">EXAMPLES</span></span>

## <span data-ttu-id="ce176-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce176-109">PARAMETERS</span></span>

### <span data-ttu-id="ce176-110">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="ce176-110">-Databases</span></span>
<span data-ttu-id="ce176-111">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ce176-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ce176-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="ce176-112">-FrequencyInterval</span></span>
<span data-ttu-id="ce176-113">Häufigkeitsintervall</span><span class="sxs-lookup"><span data-stu-id="ce176-113">Frequency Interval</span></span>

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

### <span data-ttu-id="ce176-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="ce176-114">-FrequencyUnit</span></span>
<span data-ttu-id="ce176-115">Frequenzeinheit</span><span class="sxs-lookup"><span data-stu-id="ce176-115">Frequency Unit</span></span>

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

### <span data-ttu-id="ce176-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="ce176-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="ce176-117">Mindestens eine Sicherungs Option beibehalten</span><span class="sxs-lookup"><span data-stu-id="ce176-117">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="ce176-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ce176-118">-Name</span></span>
<span data-ttu-id="ce176-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="ce176-119">WebApp Name</span></span>

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

### <span data-ttu-id="ce176-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce176-120">-ResourceGroupName</span></span>
<span data-ttu-id="ce176-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ce176-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ce176-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ce176-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ce176-123">Aufbewahrungszeitraum in Tagen</span><span class="sxs-lookup"><span data-stu-id="ce176-123">Retention Period In Days</span></span>

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

### <span data-ttu-id="ce176-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="ce176-124">-Slot</span></span>
<span data-ttu-id="ce176-125">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="ce176-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ce176-126">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="ce176-126">-StartTime</span></span>
<span data-ttu-id="ce176-127">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="ce176-127">StartTime in UTC</span></span>

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

### <span data-ttu-id="ce176-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ce176-128">-StorageAccountUrl</span></span>
<span data-ttu-id="ce176-129">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="ce176-129">Storage Account Url</span></span>

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

### <span data-ttu-id="ce176-130">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="ce176-130">-WebApp</span></span>
<span data-ttu-id="ce176-131">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="ce176-131">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce176-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce176-132">-DefaultProfile</span></span>
<span data-ttu-id="ce176-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce176-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce176-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce176-134">CommonParameters</span></span>
<span data-ttu-id="ce176-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce176-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce176-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce176-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce176-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce176-137">INPUTS</span></span>

### <span data-ttu-id="ce176-138">Website</span><span class="sxs-lookup"><span data-stu-id="ce176-138">Site</span></span>
<span data-ttu-id="ce176-139">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce176-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ce176-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce176-140">OUTPUTS</span></span>

### <span data-ttu-id="ce176-141">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce176-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ce176-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce176-142">NOTES</span></span>

## <span data-ttu-id="ce176-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce176-143">RELATED LINKS</span></span>

[<span data-ttu-id="ce176-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce176-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


