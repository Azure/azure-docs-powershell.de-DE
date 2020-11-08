---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005836"
---
# <span data-ttu-id="70ff4-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="70ff4-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="70ff4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="70ff4-103">Ruft Objekte in Azure Active Directory ab, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="70ff4-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="70ff4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70ff4-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="70ff4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="70ff4-106">Das Cmdlet " **Get-AzureRemoteAppVmStaleAdObject** " Ruft Objekte in Azure Active Directory ab, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="70ff4-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="70ff4-107">Dieses Cmdlet zeigt den Namen jedes Objekts an, das er erhält.</span><span class="sxs-lookup"><span data-stu-id="70ff4-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="70ff4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70ff4-108">EXAMPLES</span></span>

### <span data-ttu-id="70ff4-109">Beispiel 1: Abrufen veralteter Objekte für eine Sammlung</span><span class="sxs-lookup"><span data-stu-id="70ff4-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="70ff4-110">Dieser zweite Befehl ruft die veralteten Objekte für die Sammlung mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="70ff4-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="70ff4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="70ff4-111">PARAMETERS</span></span>

### <span data-ttu-id="70ff4-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="70ff4-112">-CollectionName</span></span>
<span data-ttu-id="70ff4-113">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="70ff4-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ff4-114">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="70ff4-114">-Credential</span></span>
<span data-ttu-id="70ff4-115">Gibt eine Anmeldeinformation an, die Rechte zum Ausführen dieser Aktion aufweist.</span><span class="sxs-lookup"><span data-stu-id="70ff4-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="70ff4-116">Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="70ff4-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="70ff4-117">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet die aktuellen Anmeldeinformationen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="70ff4-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ff4-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="70ff4-118">-Profile</span></span>
<span data-ttu-id="70ff4-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="70ff4-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70ff4-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="70ff4-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70ff4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ff4-121">CommonParameters</span></span>
<span data-ttu-id="70ff4-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ff4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ff4-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ff4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ff4-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70ff4-124">INPUTS</span></span>

## <span data-ttu-id="70ff4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70ff4-125">OUTPUTS</span></span>

### <span data-ttu-id="70ff4-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="70ff4-126">String</span></span>

## <span data-ttu-id="70ff4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="70ff4-127">NOTES</span></span>

## <span data-ttu-id="70ff4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70ff4-128">RELATED LINKS</span></span>

[<span data-ttu-id="70ff4-129">Löschen-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="70ff4-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


