---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005781"
---
# <span data-ttu-id="49597-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="49597-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="49597-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49597-102">SYNOPSIS</span></span>
<span data-ttu-id="49597-103">Ruft Zuordnungen von Speicherobjekten für die Standortwiederherstellung für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="49597-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="49597-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49597-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="49597-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49597-105">DESCRIPTION</span></span>
<span data-ttu-id="49597-106">Das Cmdlet " **Get-AzureSiteRecoveryStorageMapping** " Ruft Zuordnungen von Azure Site Recovery-Speicherobjekten für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="49597-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="49597-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49597-107">EXAMPLES</span></span>

### <span data-ttu-id="49597-108">Beispiel 1: Abrufen der Zuordnung zwischen einem Speicherobjekt und einem Speicherobjekt für die Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="49597-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="49597-109">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="49597-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="49597-110">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="49597-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="49597-111">Der zweite Befehl ruft die Zuordnung zwischen zwei Azure-Speicherobjekten ab.</span><span class="sxs-lookup"><span data-stu-id="49597-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="49597-112">Der Befehl gibt den primären Server für die Speicherobjekt Zuordnung als erstes Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="49597-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="49597-113">Der Befehl gibt den Server für das Wiederherstellungs Speicherobjekt als zweites Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="49597-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="49597-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="49597-114">PARAMETERS</span></span>

### <span data-ttu-id="49597-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="49597-115">-PrimaryServer</span></span>
<span data-ttu-id="49597-116">Gibt den primären Server an.</span><span class="sxs-lookup"><span data-stu-id="49597-116">Specifies the primary server.</span></span>
<span data-ttu-id="49597-117">Verwenden Sie zum Abrufen eines Servers das Cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="49597-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49597-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="49597-118">-Profile</span></span>
<span data-ttu-id="49597-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="49597-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49597-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="49597-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49597-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="49597-121">-RecoveryServer</span></span>
<span data-ttu-id="49597-122">Gibt den Wiederherstellungsserver an.</span><span class="sxs-lookup"><span data-stu-id="49597-122">Specifies the recovery server.</span></span>
<span data-ttu-id="49597-123">Verwenden Sie zum Abrufen eines Servers **Get-AzureSiteRecoveryServer**.</span><span class="sxs-lookup"><span data-stu-id="49597-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49597-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49597-124">CommonParameters</span></span>
<span data-ttu-id="49597-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49597-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49597-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49597-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49597-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49597-127">INPUTS</span></span>

## <span data-ttu-id="49597-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49597-128">OUTPUTS</span></span>

## <span data-ttu-id="49597-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="49597-129">NOTES</span></span>

## <span data-ttu-id="49597-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49597-130">RELATED LINKS</span></span>

[<span data-ttu-id="49597-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="49597-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="49597-132">Neu – AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="49597-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="49597-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="49597-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


