---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006181"
---
# <span data-ttu-id="c5aae-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="c5aae-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="c5aae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5aae-102">SYNOPSIS</span></span>
<span data-ttu-id="c5aae-103">Erstellt eine Zuordnung zwischen einem Azure-Speicherobjekt und einem Speicherobjekt für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="c5aae-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="c5aae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5aae-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5aae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5aae-105">DESCRIPTION</span></span>
<span data-ttu-id="c5aae-106">Das Cmdlet **New-AzureSiteRecoveryStorageMapping** erstellt eine Zuordnung zwischen einem Azure Azure Site Recovery Managed primäres Azure-Speicherobjekt und einem Speicherobjekt für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="c5aae-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="c5aae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5aae-107">EXAMPLES</span></span>

### <span data-ttu-id="c5aae-108">Beispiel 1: Erstellen einer Zuordnung zwischen einem Speicherobjekt und einem Speicherobjekt für die Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="c5aae-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="c5aae-109">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="c5aae-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="c5aae-110">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="c5aae-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="c5aae-111">Der zweite Befehl ruft den Standort Wiederherstellungs Speicher für den ersten Server im $Servers-Array ab und speichert ihn dann im $Storages.</span><span class="sxs-lookup"><span data-stu-id="c5aae-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="c5aae-112">Der endgültige Befehl erstellt eine Zuordnung zwischen dem primären Netzwerk und dem Wiederherstellungs Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c5aae-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="c5aae-113">Der Befehl gibt das primäre Speicherobjekt als erstes Element von $Storages an.</span><span class="sxs-lookup"><span data-stu-id="c5aae-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="c5aae-114">Der Befehl gibt das Speicherobjekt für die Wiederherstellung als zweites Element von $Storages an.</span><span class="sxs-lookup"><span data-stu-id="c5aae-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="c5aae-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5aae-115">PARAMETERS</span></span>

### <span data-ttu-id="c5aae-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="c5aae-116">-PrimaryStorage</span></span>
<span data-ttu-id="c5aae-117">Gibt den primären Speicher an, der dem Wiederherstellungs Speicher zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5aae-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="c5aae-118">Verwenden Sie das Get-AzureSiteRecoveryStorage-Cmdlet, um ein **ASRStorage** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5aae-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aae-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5aae-119">-Profile</span></span>
<span data-ttu-id="c5aae-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c5aae-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5aae-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c5aae-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aae-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="c5aae-122">-RecoveryStorage</span></span>
<span data-ttu-id="c5aae-123">Gibt das Speicherobjekt für die Wiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="c5aae-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="c5aae-124">Dieses Cmdlet ordnet das primäre Speicherobjekt dem Speicherobjekt zu, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c5aae-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="c5aae-125">Verwenden **Sie Get-AzureSiteRecoveryStorage** , um ein **ASRStorage** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5aae-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5aae-126">CommonParameters</span></span>
<span data-ttu-id="c5aae-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5aae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5aae-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5aae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5aae-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5aae-129">INPUTS</span></span>

## <span data-ttu-id="c5aae-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5aae-130">OUTPUTS</span></span>

## <span data-ttu-id="c5aae-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5aae-131">NOTES</span></span>

## <span data-ttu-id="c5aae-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5aae-132">RELATED LINKS</span></span>

[<span data-ttu-id="c5aae-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="c5aae-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="c5aae-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="c5aae-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="c5aae-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="c5aae-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


