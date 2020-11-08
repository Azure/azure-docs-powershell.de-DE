---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006519"
---
# <span data-ttu-id="88d51-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="88d51-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="88d51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88d51-102">SYNOPSIS</span></span>
<span data-ttu-id="88d51-103">Ruft eine Routentabelle ab.</span><span class="sxs-lookup"><span data-stu-id="88d51-103">Gets a route table.</span></span>

## <span data-ttu-id="88d51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88d51-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="88d51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88d51-105">DESCRIPTION</span></span>
<span data-ttu-id="88d51-106">Das Cmdlet " **Get-AzureRouteTable** " Ruft eine Routingtabelle ab.</span><span class="sxs-lookup"><span data-stu-id="88d51-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="88d51-107">Geben Sie den *detaillierten* Parameter an, um die Routen in der Route-Tabelle aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="88d51-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="88d51-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88d51-108">EXAMPLES</span></span>

### <span data-ttu-id="88d51-109">Beispiel 1: Abrufen von Details zu einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="88d51-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="88d51-110">Dieser Befehl ruft die Details einer Routentabelle mit dem Namen ApplianceRouteTable ab.</span><span class="sxs-lookup"><span data-stu-id="88d51-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="88d51-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="88d51-111">PARAMETERS</span></span>

### <span data-ttu-id="88d51-112">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="88d51-112">-Detailed</span></span>
<span data-ttu-id="88d51-113">Gibt an, dass dieses Cmdlet die Routen in der Route-Tabelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="88d51-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d51-114">-Name</span><span class="sxs-lookup"><span data-stu-id="88d51-114">-Name</span></span>
<span data-ttu-id="88d51-115">Gibt den Namen der Arbeitsplan Tabelle an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="88d51-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="88d51-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="88d51-116">-Profile</span></span>
<span data-ttu-id="88d51-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="88d51-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="88d51-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="88d51-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88d51-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d51-119">CommonParameters</span></span>
<span data-ttu-id="88d51-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88d51-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d51-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d51-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d51-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88d51-122">INPUTS</span></span>

## <span data-ttu-id="88d51-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88d51-123">OUTPUTS</span></span>

## <span data-ttu-id="88d51-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="88d51-124">NOTES</span></span>

## <span data-ttu-id="88d51-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88d51-125">RELATED LINKS</span></span>

[<span data-ttu-id="88d51-126">Neu – AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="88d51-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="88d51-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="88d51-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


