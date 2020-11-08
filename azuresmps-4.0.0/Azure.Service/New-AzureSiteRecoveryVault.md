---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006180"
---
# <span data-ttu-id="be986-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="be986-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="be986-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be986-102">SYNOPSIS</span></span>
<span data-ttu-id="be986-103">Erstellt einen Vault für Website Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="be986-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="be986-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be986-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="be986-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be986-105">DESCRIPTION</span></span>
<span data-ttu-id="be986-106">Mit dem Cmdlet **New-AzureSiteRecoveryVault** wird ein Azure Site Recovery Services Vault erstellt.</span><span class="sxs-lookup"><span data-stu-id="be986-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="be986-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be986-107">EXAMPLES</span></span>

### <span data-ttu-id="be986-108">Beispiel 1: Erstellen eines Tresors</span><span class="sxs-lookup"><span data-stu-id="be986-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="be986-109">Mit diesem Befehl wird ein Tresor mit dem Namen ContosoVault im West US-Standort erstellt.</span><span class="sxs-lookup"><span data-stu-id="be986-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="be986-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be986-110">PARAMETERS</span></span>

### <span data-ttu-id="be986-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="be986-111">-Location</span></span>
<span data-ttu-id="be986-112">Gibt den geografischen Standort an.</span><span class="sxs-lookup"><span data-stu-id="be986-112">Specifies the geographical location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be986-113">-Name</span><span class="sxs-lookup"><span data-stu-id="be986-113">-Name</span></span>
<span data-ttu-id="be986-114">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="be986-114">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be986-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="be986-115">-Profile</span></span>
<span data-ttu-id="be986-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="be986-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be986-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="be986-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="be986-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be986-118">CommonParameters</span></span>
<span data-ttu-id="be986-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be986-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be986-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be986-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be986-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be986-121">INPUTS</span></span>

## <span data-ttu-id="be986-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be986-122">OUTPUTS</span></span>

## <span data-ttu-id="be986-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="be986-123">NOTES</span></span>

## <span data-ttu-id="be986-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be986-124">RELATED LINKS</span></span>

[<span data-ttu-id="be986-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="be986-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


