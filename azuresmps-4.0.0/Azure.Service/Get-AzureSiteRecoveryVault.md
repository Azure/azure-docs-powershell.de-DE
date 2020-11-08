---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006771"
---
# <span data-ttu-id="cab18-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="cab18-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="cab18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cab18-102">SYNOPSIS</span></span>
<span data-ttu-id="cab18-103">Ruft Website-Wiederherstellungs Depots aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="cab18-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="cab18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cab18-104">SYNTAX</span></span>

### <span data-ttu-id="cab18-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="cab18-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cab18-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cab18-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cab18-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cab18-107">DESCRIPTION</span></span>
<span data-ttu-id="cab18-108">Das Cmdlet " **Get-AzureSiteRecoveryVault** " Ruft eine Liste der Azure Site Recovery Vaults oder eines bestimmten Standort Wiederherstellungs Depots aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="cab18-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="cab18-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cab18-109">EXAMPLES</span></span>

### <span data-ttu-id="cab18-110">Beispiel 1: Abrufen des aktiven Tresors</span><span class="sxs-lookup"><span data-stu-id="cab18-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="cab18-111">Dieser Befehl ruft das Active Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="cab18-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="cab18-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cab18-112">PARAMETERS</span></span>

### <span data-ttu-id="cab18-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cab18-113">-Name</span></span>
<span data-ttu-id="cab18-114">Gibt den Namen des abzurufenden Tresors an.</span><span class="sxs-lookup"><span data-stu-id="cab18-114">Specifies the name of the vault to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab18-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="cab18-115">-Profile</span></span>
<span data-ttu-id="cab18-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="cab18-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cab18-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="cab18-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cab18-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab18-118">CommonParameters</span></span>
<span data-ttu-id="cab18-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab18-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab18-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab18-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab18-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cab18-121">INPUTS</span></span>

## <span data-ttu-id="cab18-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cab18-122">OUTPUTS</span></span>

## <span data-ttu-id="cab18-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="cab18-123">NOTES</span></span>

## <span data-ttu-id="cab18-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cab18-124">RELATED LINKS</span></span>

[<span data-ttu-id="cab18-125">Neu – AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="cab18-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


