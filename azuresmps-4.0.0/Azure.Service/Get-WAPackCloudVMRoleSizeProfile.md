---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006714"
---
# <span data-ttu-id="a36a6-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="a36a6-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="a36a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a36a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a36a6-103">Ruft Cloud VM-Rollengröße-Profilobjekte ab.</span><span class="sxs-lookup"><span data-stu-id="a36a6-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="a36a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a36a6-104">SYNTAX</span></span>

### <span data-ttu-id="a36a6-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="a36a6-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a36a6-106">FromName</span><span class="sxs-lookup"><span data-stu-id="a36a6-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a36a6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a36a6-107">DESCRIPTION</span></span>
<span data-ttu-id="a36a6-108">Das Cmdlet " **Get-WAPackCloudVMRoleSizeProfile** " ruft Cloud VM-Rollengröße-Profilobjekte für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a36a6-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="a36a6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a36a6-109">EXAMPLES</span></span>

### <span data-ttu-id="a36a6-110">Beispiel 1: Abrufen eines VM-Rollen Formats für eine Cloud mit einem Namen</span><span class="sxs-lookup"><span data-stu-id="a36a6-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="a36a6-111">Dieser Befehl ruft das Größen Profil mit dem Namen klein ab.</span><span class="sxs-lookup"><span data-stu-id="a36a6-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="a36a6-112">Beispiel 2: Abrufen aller Rollenformat Profile für die VM-Cloud</span><span class="sxs-lookup"><span data-stu-id="a36a6-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="a36a6-113">Dieser Befehl ruft alle Größen Profile ab.</span><span class="sxs-lookup"><span data-stu-id="a36a6-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="a36a6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a36a6-114">PARAMETERS</span></span>

### <span data-ttu-id="a36a6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a36a6-115">-Name</span></span>
<span data-ttu-id="a36a6-116">Gibt den Namen eines VM-Rollengrößen Profils für die Cloud an.</span><span class="sxs-lookup"><span data-stu-id="a36a6-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36a6-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a36a6-117">-Profile</span></span>
<span data-ttu-id="a36a6-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a36a6-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a36a6-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a36a6-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a36a6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36a6-120">CommonParameters</span></span>
<span data-ttu-id="a36a6-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a36a6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36a6-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a36a6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36a6-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a36a6-123">INPUTS</span></span>

## <span data-ttu-id="a36a6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a36a6-124">OUTPUTS</span></span>

## <span data-ttu-id="a36a6-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a36a6-125">NOTES</span></span>

## <span data-ttu-id="a36a6-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a36a6-126">RELATED LINKS</span></span>

[<span data-ttu-id="a36a6-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a36a6-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


