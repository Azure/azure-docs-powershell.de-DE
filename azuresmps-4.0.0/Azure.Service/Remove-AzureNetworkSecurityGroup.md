---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006360"
---
# <span data-ttu-id="f5dd3-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f5dd3-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="f5dd3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="f5dd3-103">Löscht eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-103">Deletes a network security group.</span></span>

## <span data-ttu-id="f5dd3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5dd3-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5dd3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5dd3-105">DESCRIPTION</span></span>
<span data-ttu-id="f5dd3-106">Das Cmdlet **Remove-AzureNetworkSecurityGroup** löscht eine Azure Network Security-Gruppe aus Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="f5dd3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5dd3-107">EXAMPLES</span></span>

## <span data-ttu-id="f5dd3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5dd3-108">PARAMETERS</span></span>

### <span data-ttu-id="f5dd3-109">-Force</span><span class="sxs-lookup"><span data-stu-id="f5dd3-109">-Force</span></span>
<span data-ttu-id="f5dd3-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5dd3-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f5dd3-111">-Name</span></span>
<span data-ttu-id="f5dd3-112">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f5dd3-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5dd3-113">-PassThru</span></span>
<span data-ttu-id="f5dd3-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f5dd3-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5dd3-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="f5dd3-116">-Profile</span></span>
<span data-ttu-id="f5dd3-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f5dd3-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5dd3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5dd3-119">CommonParameters</span></span>
<span data-ttu-id="f5dd3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5dd3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5dd3-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5dd3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5dd3-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5dd3-122">INPUTS</span></span>

## <span data-ttu-id="f5dd3-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5dd3-123">OUTPUTS</span></span>

## <span data-ttu-id="f5dd3-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5dd3-124">NOTES</span></span>

## <span data-ttu-id="f5dd3-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5dd3-125">RELATED LINKS</span></span>

[<span data-ttu-id="f5dd3-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f5dd3-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="f5dd3-127">Neu – AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f5dd3-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


