---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006341"
---
# <span data-ttu-id="4156a-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="4156a-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="4156a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4156a-102">SYNOPSIS</span></span>
<span data-ttu-id="4156a-103">Entfernt eine Route aus einer Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4156a-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="4156a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4156a-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4156a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4156a-105">DESCRIPTION</span></span>
<span data-ttu-id="4156a-106">Das Cmdlet **Remove-AzureRoute** entfernt eine Route aus einer Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4156a-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="4156a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4156a-107">EXAMPLES</span></span>

### <span data-ttu-id="4156a-108">Beispiel 1: Entfernen einer Route</span><span class="sxs-lookup"><span data-stu-id="4156a-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="4156a-109">Dieser Befehl ruft eine Routentabelle mit dem Namen ApplianceRouteTable ab.</span><span class="sxs-lookup"><span data-stu-id="4156a-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="4156a-110">Der Befehl übergibt diese Routingtabelle an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4156a-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="4156a-111">Das aktuelle Cmdlet entfernt eine Route mit dem Namen InternetRoute.</span><span class="sxs-lookup"><span data-stu-id="4156a-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="4156a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4156a-112">PARAMETERS</span></span>

### <span data-ttu-id="4156a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4156a-113">-Force</span></span>
<span data-ttu-id="4156a-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4156a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4156a-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="4156a-115">-Profile</span></span>
<span data-ttu-id="4156a-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4156a-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4156a-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4156a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4156a-118">-Routename</span><span class="sxs-lookup"><span data-stu-id="4156a-118">-RouteName</span></span>
<span data-ttu-id="4156a-119">Gibt einen Namen für die neue Route an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4156a-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4156a-120">-Routel</span><span class="sxs-lookup"><span data-stu-id="4156a-120">-RouteTable</span></span>
<span data-ttu-id="4156a-121">Gibt die Route-Tabelle an, aus der dieses Cmdlet eine Route entfernt.</span><span class="sxs-lookup"><span data-stu-id="4156a-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4156a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4156a-122">CommonParameters</span></span>
<span data-ttu-id="4156a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4156a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4156a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4156a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4156a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4156a-125">INPUTS</span></span>

## <span data-ttu-id="4156a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4156a-126">OUTPUTS</span></span>

## <span data-ttu-id="4156a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4156a-127">NOTES</span></span>

## <span data-ttu-id="4156a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4156a-128">RELATED LINKS</span></span>

[<span data-ttu-id="4156a-129">Satz-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="4156a-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


