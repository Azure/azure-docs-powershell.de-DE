---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005985"
---
# <span data-ttu-id="6c00d-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c00d-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="6c00d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c00d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c00d-103">Startet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6c00d-103">Starts an application gateway.</span></span>

## <span data-ttu-id="6c00d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c00d-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6c00d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c00d-105">DESCRIPTION</span></span>
<span data-ttu-id="6c00d-106">Das **Start-AzureApplicationGateway-** Cmdlet startet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6c00d-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="6c00d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c00d-107">EXAMPLES</span></span>

### <span data-ttu-id="6c00d-108">Beispiel 1: Starten eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="6c00d-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="6c00d-109">Mit diesem Befehl wird das Anwendungsgateway mit dem Namen ApplicationGateway06 gestartet.</span><span class="sxs-lookup"><span data-stu-id="6c00d-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="6c00d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c00d-110">PARAMETERS</span></span>

### <span data-ttu-id="6c00d-111">-Name</span><span class="sxs-lookup"><span data-stu-id="6c00d-111">-Name</span></span>
<span data-ttu-id="6c00d-112">Gibt den Namen des Anwendungs Gateways an, das mit diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6c00d-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="6c00d-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c00d-113">-Profile</span></span>
<span data-ttu-id="6c00d-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6c00d-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6c00d-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6c00d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c00d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c00d-116">CommonParameters</span></span>
<span data-ttu-id="6c00d-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c00d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c00d-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c00d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c00d-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c00d-119">INPUTS</span></span>

### <span data-ttu-id="6c00d-120">System. String</span><span class="sxs-lookup"><span data-stu-id="6c00d-120">System.String</span></span>

## <span data-ttu-id="6c00d-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c00d-121">OUTPUTS</span></span>

### <span data-ttu-id="6c00d-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6c00d-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="6c00d-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c00d-123">NOTES</span></span>

## <span data-ttu-id="6c00d-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c00d-124">RELATED LINKS</span></span>

[<span data-ttu-id="6c00d-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c00d-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="6c00d-126">Neu – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c00d-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="6c00d-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c00d-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="6c00d-128">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c00d-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="6c00d-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c00d-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


