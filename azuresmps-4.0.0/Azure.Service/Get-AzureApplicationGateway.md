---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005876"
---
# <span data-ttu-id="39012-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39012-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="39012-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39012-102">SYNOPSIS</span></span>
<span data-ttu-id="39012-103">Ruft ein Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="39012-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="39012-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39012-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39012-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39012-105">DESCRIPTION</span></span>
<span data-ttu-id="39012-106">Das Cmdlet " **Get-AzureApplicationGateway** " Ruft ein vorhandenes Azure Application-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="39012-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="39012-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39012-107">EXAMPLES</span></span>

### <span data-ttu-id="39012-108">Beispiel 1: Abrufen eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="39012-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="39012-109">Dieser Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway06 ab.</span><span class="sxs-lookup"><span data-stu-id="39012-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="39012-110">Beispiel 2: Abrufen aller Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="39012-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="39012-111">Dieser Befehl ruft alle Anwendungs Gateways unter Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="39012-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="39012-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="39012-112">PARAMETERS</span></span>

### <span data-ttu-id="39012-113">-Name</span><span class="sxs-lookup"><span data-stu-id="39012-113">-Name</span></span>
<span data-ttu-id="39012-114">Gibt den Namen des Anwendungs Gateways an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="39012-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39012-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="39012-115">-Profile</span></span>
<span data-ttu-id="39012-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="39012-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="39012-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="39012-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39012-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39012-118">CommonParameters</span></span>
<span data-ttu-id="39012-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39012-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39012-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39012-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39012-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39012-121">INPUTS</span></span>

### <span data-ttu-id="39012-122">System. String</span><span class="sxs-lookup"><span data-stu-id="39012-122">System.String</span></span>

## <span data-ttu-id="39012-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39012-123">OUTPUTS</span></span>

### <span data-ttu-id="39012-124">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway></span><span class="sxs-lookup"><span data-stu-id="39012-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="39012-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="39012-125">NOTES</span></span>

## <span data-ttu-id="39012-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39012-126">RELATED LINKS</span></span>

[<span data-ttu-id="39012-127">Neu – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39012-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="39012-128">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39012-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="39012-129">Anfang-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39012-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="39012-130">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39012-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="39012-131">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39012-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


