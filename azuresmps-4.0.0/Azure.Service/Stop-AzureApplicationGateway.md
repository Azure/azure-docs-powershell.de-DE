---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006614"
---
# <span data-ttu-id="b4866-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4866-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="b4866-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4866-102">SYNOPSIS</span></span>
<span data-ttu-id="b4866-103">Beendet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b4866-103">Stops an application gateway.</span></span>

## <span data-ttu-id="b4866-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4866-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b4866-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4866-105">DESCRIPTION</span></span>
<span data-ttu-id="b4866-106">Das Cmdlet **Stop-AzureApplicationGateway** beendet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b4866-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="b4866-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4866-107">EXAMPLES</span></span>

### <span data-ttu-id="b4866-108">Beispiel 1: Beenden eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="b4866-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="b4866-109">Dieser Befehl beendet das Anwendungsgateway mit dem Namen ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="b4866-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="b4866-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4866-110">PARAMETERS</span></span>

### <span data-ttu-id="b4866-111">-Name</span><span class="sxs-lookup"><span data-stu-id="b4866-111">-Name</span></span>
<span data-ttu-id="b4866-112">Gibt den Namen des Anwendungs Gateways an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4866-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b4866-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4866-113">-Profile</span></span>
<span data-ttu-id="b4866-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b4866-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4866-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b4866-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4866-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4866-116">CommonParameters</span></span>
<span data-ttu-id="b4866-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4866-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4866-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4866-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4866-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4866-119">INPUTS</span></span>

### <span data-ttu-id="b4866-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b4866-120">System.String</span></span>

## <span data-ttu-id="b4866-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4866-121">OUTPUTS</span></span>

### <span data-ttu-id="b4866-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b4866-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="b4866-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4866-123">NOTES</span></span>

## <span data-ttu-id="b4866-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4866-124">RELATED LINKS</span></span>

[<span data-ttu-id="b4866-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4866-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="b4866-126">Neu – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4866-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="b4866-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4866-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="b4866-128">Anfang-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4866-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="b4866-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4866-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
