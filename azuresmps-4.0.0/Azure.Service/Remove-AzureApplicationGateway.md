---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006703"
---
# <span data-ttu-id="34dc1-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34dc1-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="34dc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="34dc1-103">Entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="34dc1-103">Removes an application gateway.</span></span>

## <span data-ttu-id="34dc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34dc1-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34dc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="34dc1-106">Das Cmdlet **Remove-AzureApplicationGateway** entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="34dc1-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="34dc1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34dc1-107">EXAMPLES</span></span>

### <span data-ttu-id="34dc1-108">Beispiel 1: Entfernen eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="34dc1-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="34dc1-109">Mit diesem Befehl wird das Anwendungsgateway mit dem Namen ApplicationGateway06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="34dc1-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="34dc1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34dc1-110">PARAMETERS</span></span>

### <span data-ttu-id="34dc1-111">-Name</span><span class="sxs-lookup"><span data-stu-id="34dc1-111">-Name</span></span>
<span data-ttu-id="34dc1-112">Gibt den Namen des Anwendungs Gateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="34dc1-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34dc1-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="34dc1-113">-Profile</span></span>
<span data-ttu-id="34dc1-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="34dc1-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="34dc1-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="34dc1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34dc1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34dc1-116">CommonParameters</span></span>
<span data-ttu-id="34dc1-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34dc1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34dc1-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34dc1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34dc1-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34dc1-119">INPUTS</span></span>

### <span data-ttu-id="34dc1-120">System. String</span><span class="sxs-lookup"><span data-stu-id="34dc1-120">System.String</span></span>

## <span data-ttu-id="34dc1-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34dc1-121">OUTPUTS</span></span>

### <span data-ttu-id="34dc1-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="34dc1-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="34dc1-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="34dc1-123">NOTES</span></span>

## <span data-ttu-id="34dc1-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34dc1-124">RELATED LINKS</span></span>

[<span data-ttu-id="34dc1-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34dc1-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="34dc1-126">Neu – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34dc1-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="34dc1-127">Anfang-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34dc1-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="34dc1-128">Stopp-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34dc1-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="34dc1-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34dc1-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


