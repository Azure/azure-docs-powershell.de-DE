---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006777"
---
# <span data-ttu-id="adceb-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="adceb-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="adceb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="adceb-102">SYNOPSIS</span></span>
<span data-ttu-id="adceb-103">Ruft die virtuellen Computer in einer Azure RemoteApp-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="adceb-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="adceb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="adceb-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="adceb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adceb-105">DESCRIPTION</span></span>
<span data-ttu-id="adceb-106">Das Cmdlet " **Get-AzureRemoteAppVM** " Ruft die virtuellen Computer ab, die unter einer Azure RemoteApp-Sammlung für das Sitzungs Hosting erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="adceb-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="adceb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="adceb-107">EXAMPLES</span></span>

### <span data-ttu-id="adceb-108">Beispiel 1: Anzeigen der virtuellen Computer in einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="adceb-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="adceb-109">Dieser Befehl zeigt die für das Sitzungs Hosting verwendeten virtuellen Computer in einer Azure RemoteApp-Sammlung mit dem Namen "Contoso" an.</span><span class="sxs-lookup"><span data-stu-id="adceb-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="adceb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="adceb-110">PARAMETERS</span></span>

### <span data-ttu-id="adceb-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="adceb-111">-CollectionName</span></span>
<span data-ttu-id="adceb-112">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="adceb-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="adceb-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="adceb-113">-Profile</span></span>
<span data-ttu-id="adceb-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="adceb-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="adceb-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="adceb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="adceb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adceb-116">CommonParameters</span></span>
<span data-ttu-id="adceb-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adceb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adceb-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adceb-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adceb-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="adceb-119">INPUTS</span></span>

## <span data-ttu-id="adceb-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="adceb-120">OUTPUTS</span></span>

## <span data-ttu-id="adceb-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="adceb-121">NOTES</span></span>

## <span data-ttu-id="adceb-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="adceb-122">RELATED LINKS</span></span>

[<span data-ttu-id="adceb-123">Neustart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="adceb-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


