---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006195"
---
# <span data-ttu-id="41dc7-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="41dc7-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="41dc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="41dc7-103">Erstellt eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="41dc7-103">Creates a route table.</span></span>

## <span data-ttu-id="41dc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41dc7-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="41dc7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="41dc7-106">Das Cmdlet **New-AzureRouteTable** erstellt eine Routingtabelle an einem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="41dc7-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="41dc7-107">Sie können der Route-Tabelle benutzerdefinierte Routen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="41dc7-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="41dc7-108">Sie können die Routingtabelle einem Subnetz in einem virtuellen Netzwerk zuordnen.</span><span class="sxs-lookup"><span data-stu-id="41dc7-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="41dc7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41dc7-109">EXAMPLES</span></span>

## <span data-ttu-id="41dc7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="41dc7-110">PARAMETERS</span></span>

### <span data-ttu-id="41dc7-111">-Label</span><span class="sxs-lookup"><span data-stu-id="41dc7-111">-Label</span></span>
<span data-ttu-id="41dc7-112">Gibt eine Beschreibung für die neue Arbeitsplan Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="41dc7-112">Specifies a description for the new route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41dc7-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="41dc7-113">-Location</span></span>
<span data-ttu-id="41dc7-114">Gibt den Speicherort an, an dem dieses Cmdlet die Route-Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="41dc7-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="41dc7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="41dc7-115">-Name</span></span>
<span data-ttu-id="41dc7-116">Gibt einen Namen für die von diesem Cmdlet erstellte Routingtabelle an.</span><span class="sxs-lookup"><span data-stu-id="41dc7-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="41dc7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="41dc7-117">-Profile</span></span>
<span data-ttu-id="41dc7-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="41dc7-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="41dc7-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="41dc7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41dc7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41dc7-120">CommonParameters</span></span>
<span data-ttu-id="41dc7-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41dc7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41dc7-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41dc7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41dc7-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41dc7-123">INPUTS</span></span>

## <span data-ttu-id="41dc7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41dc7-124">OUTPUTS</span></span>

## <span data-ttu-id="41dc7-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="41dc7-125">NOTES</span></span>

## <span data-ttu-id="41dc7-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41dc7-126">RELATED LINKS</span></span>

[<span data-ttu-id="41dc7-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="41dc7-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="41dc7-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="41dc7-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


