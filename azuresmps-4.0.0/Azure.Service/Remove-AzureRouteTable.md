---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006338"
---
# <span data-ttu-id="d58bf-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="d58bf-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="d58bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d58bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d58bf-103">Entfernt eine Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d58bf-103">Removes a route table.</span></span>

## <span data-ttu-id="d58bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d58bf-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d58bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d58bf-105">DESCRIPTION</span></span>
<span data-ttu-id="d58bf-106">Das Cmdlet **Remove-AzureRouteTable** entfernt eine Route-Tabelle aus Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d58bf-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="d58bf-107">Wenn eine Routentabelle einem Subnetz zugeordnet ist, können Sie die Tabelle nicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="d58bf-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="d58bf-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d58bf-108">EXAMPLES</span></span>

### <span data-ttu-id="d58bf-109">Beispiel 1: Entfernen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="d58bf-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="d58bf-110">Dieser Befehl entfernt die Route-Tabelle mit dem Namen PublicRouteTable.</span><span class="sxs-lookup"><span data-stu-id="d58bf-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="d58bf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d58bf-111">PARAMETERS</span></span>

### <span data-ttu-id="d58bf-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d58bf-112">-Force</span></span>
<span data-ttu-id="d58bf-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d58bf-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d58bf-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d58bf-114">-Name</span></span>
<span data-ttu-id="d58bf-115">Gibt den Namen der Arbeitsplan Tabelle an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d58bf-115">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58bf-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d58bf-116">-PassThru</span></span>
<span data-ttu-id="d58bf-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d58bf-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d58bf-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d58bf-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d58bf-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="d58bf-119">-Profile</span></span>
<span data-ttu-id="d58bf-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d58bf-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d58bf-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d58bf-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d58bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58bf-122">CommonParameters</span></span>
<span data-ttu-id="d58bf-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58bf-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58bf-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d58bf-125">INPUTS</span></span>

## <span data-ttu-id="d58bf-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d58bf-126">OUTPUTS</span></span>

## <span data-ttu-id="d58bf-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d58bf-127">NOTES</span></span>

## <span data-ttu-id="d58bf-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d58bf-128">RELATED LINKS</span></span>

[<span data-ttu-id="d58bf-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="d58bf-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="d58bf-130">Neu – AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="d58bf-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
