---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475209"
---
# <span data-ttu-id="7ac0e-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="7ac0e-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="7ac0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ac0e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac0e-103">Lädt Azure-Authentifizierungsinformationen aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="7ac0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ac0e-104">SYNTAX</span></span>

### <span data-ttu-id="7ac0e-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="7ac0e-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="7ac0e-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="7ac0e-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="7ac0e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ac0e-107">DESCRIPTION</span></span>
<span data-ttu-id="7ac0e-108">Das Select-AzureRmProfile-Cmdlet lädt Authentifizierungsinformationen aus einer Datei, um die Azure-Umgebung und den Kontext zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="7ac0e-109">Cmdlets, die Sie in der aktuellen Sitzung ausführen, verwenden diese Informationen, um Anforderungen an den Azure Resource Manager zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="7ac0e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ac0e-110">EXAMPLES</span></span>

### <span data-ttu-id="7ac0e-111">Beispiel 1: Auswählen eines Profils aus einem PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="7ac0e-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="7ac0e-112">In diesem Beispiel wird ein Profil aus einem PSAzureProfile ausgewählt, das an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="7ac0e-113">Beispiel 2: Auswählen eines Profils aus einer JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="7ac0e-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="7ac0e-114">In diesem Beispiel wird ein Profil aus einer JSON-Datei ausgewählt, die an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="7ac0e-115">Diese JSON-Datei kann aus Save-AzureRmProfile erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="7ac0e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ac0e-116">PARAMETERS</span></span>

### <span data-ttu-id="7ac0e-117">-Path</span><span class="sxs-lookup"><span data-stu-id="7ac0e-117">-Path</span></span>
<span data-ttu-id="7ac0e-118">Gibt den Pfad zu Profilinformationen an, die mithilfe von Save-AzureRMProfile gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac0e-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="7ac0e-119">-Profile</span></span>
<span data-ttu-id="7ac0e-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ac0e-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac0e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac0e-122">CommonParameters</span></span>
<span data-ttu-id="7ac0e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac0e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac0e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac0e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac0e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ac0e-125">INPUTS</span></span>

## <span data-ttu-id="7ac0e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ac0e-126">OUTPUTS</span></span>

### <span data-ttu-id="7ac0e-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="7ac0e-127">PSAzureProfile</span></span>

## <span data-ttu-id="7ac0e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ac0e-128">NOTES</span></span>

## <span data-ttu-id="7ac0e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ac0e-129">RELATED LINKS</span></span>

[<span data-ttu-id="7ac0e-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="7ac0e-130">Get-AzureRMContext</span></span>]()

