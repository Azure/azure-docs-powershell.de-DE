---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006315"
---
# <span data-ttu-id="60df6-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="60df6-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="60df6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60df6-102">SYNOPSIS</span></span>
<span data-ttu-id="60df6-103">Entfernt eine Speicherobjekt Zuordnung für einen Standort Wiederherstellungs Tresor.</span><span class="sxs-lookup"><span data-stu-id="60df6-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="60df6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60df6-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="60df6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60df6-105">DESCRIPTION</span></span>
<span data-ttu-id="60df6-106">Das Cmdlet **Remove-AzureSiteRecoveryStorageMapping** entfernt eine Speicherobjekt Zuordnung für das aktuelle Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="60df6-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="60df6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60df6-107">EXAMPLES</span></span>

### <span data-ttu-id="60df6-108">Beispiel 1: Entfernen der Zuordnung zwischen einem Netzwerk und einem Wiederherstellungs Netzwerk</span><span class="sxs-lookup"><span data-stu-id="60df6-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="60df6-109">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="60df6-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="60df6-110">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="60df6-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="60df6-111">Der zweite Befehl ruft die Zuordnung zwischen zwei Speicherobjekten ab und speichert Sie dann in der $StorageMapping Variablen.</span><span class="sxs-lookup"><span data-stu-id="60df6-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="60df6-112">Der Befehl gibt den primären Server für die Netzwerkzuordnung als erstes Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="60df6-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="60df6-113">Der Befehl gibt den Server für das Wiederherstellungs Netzwerk als zweites Element von $Servers an.</span><span class="sxs-lookup"><span data-stu-id="60df6-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="60df6-114">Der endgültige Befehl entfernt die Zuordnung in $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="60df6-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="60df6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="60df6-115">PARAMETERS</span></span>

### <span data-ttu-id="60df6-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="60df6-116">-Profile</span></span>
<span data-ttu-id="60df6-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="60df6-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="60df6-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="60df6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="60df6-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="60df6-119">-StorageMapping</span></span>
<span data-ttu-id="60df6-120">Gibt eine Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="60df6-120">Specifies a network mapping.</span></span>
<span data-ttu-id="60df6-121">Verwenden Sie zum Abrufen eines **ASRStorageMapping** das Cmdlet **Get-AzureSiteRecoveryStorage** .</span><span class="sxs-lookup"><span data-stu-id="60df6-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60df6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60df6-122">CommonParameters</span></span>
<span data-ttu-id="60df6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60df6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60df6-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60df6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60df6-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60df6-125">INPUTS</span></span>

## <span data-ttu-id="60df6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60df6-126">OUTPUTS</span></span>

## <span data-ttu-id="60df6-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="60df6-127">NOTES</span></span>

## <span data-ttu-id="60df6-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60df6-128">RELATED LINKS</span></span>

[<span data-ttu-id="60df6-129">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="60df6-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


