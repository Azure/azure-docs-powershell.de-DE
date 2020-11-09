---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301984"
---
# <span data-ttu-id="b9e41-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b9e41-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b9e41-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9e41-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e41-103">Erstellt eine Übereinstimmungs Variable für die Firewall-Bedingung.</span><span class="sxs-lookup"><span data-stu-id="b9e41-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b9e41-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9e41-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9e41-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9e41-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e41-106">Das **New-AzApplicationGatewayFirewallMatchVariable** erstellt eine Übereinstimmungs Variable für die Firewall-Bedingung.</span><span class="sxs-lookup"><span data-stu-id="b9e41-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b9e41-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9e41-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e41-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9e41-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="b9e41-109">Der Befehl erstellt eine neue Übereinstimmungs Variable mit dem Namen der Anforderungs Kopfzeilen und der Auswahl ist Inhaltslängen Feld.</span><span class="sxs-lookup"><span data-stu-id="b9e41-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="b9e41-110">Die neue Übereinstimmungs Variable wird in $Variable gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b9e41-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="b9e41-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9e41-111">PARAMETERS</span></span>

### <span data-ttu-id="b9e41-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e41-112">-DefaultProfile</span></span>
<span data-ttu-id="b9e41-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9e41-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e41-114">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="b9e41-114">-Selector</span></span>
<span data-ttu-id="b9e41-115">Beschreibt das Feld der matchVariable-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="b9e41-115">Describes field of the matchVariable collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e41-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="b9e41-116">-VariableName</span></span>
<span data-ttu-id="b9e41-117">Variable vergleichen.</span><span class="sxs-lookup"><span data-stu-id="b9e41-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e41-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e41-118">CommonParameters</span></span>
<span data-ttu-id="b9e41-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e41-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e41-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e41-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e41-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9e41-121">INPUTS</span></span>

### <span data-ttu-id="b9e41-122">Keine</span><span class="sxs-lookup"><span data-stu-id="b9e41-122">None</span></span>

## <span data-ttu-id="b9e41-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9e41-123">OUTPUTS</span></span>

### <span data-ttu-id="b9e41-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b9e41-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b9e41-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9e41-125">NOTES</span></span>

## <span data-ttu-id="b9e41-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9e41-126">RELATED LINKS</span></span>
