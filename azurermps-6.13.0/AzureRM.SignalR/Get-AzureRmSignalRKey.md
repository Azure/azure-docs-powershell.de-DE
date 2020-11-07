---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662920"
---
# <span data-ttu-id="52b57-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="52b57-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="52b57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52b57-102">SYNOPSIS</span></span>
<span data-ttu-id="52b57-103">Rufen Sie die Zugriffstasten eines Signalisierungs Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="52b57-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52b57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52b57-104">SYNTAX</span></span>

### <span data-ttu-id="52b57-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="52b57-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52b57-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b57-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b57-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b57-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52b57-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52b57-108">DESCRIPTION</span></span>
<span data-ttu-id="52b57-109">Rufen Sie die Zugriffstasten eines Signalisierungs Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="52b57-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="52b57-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52b57-110">EXAMPLES</span></span>

### <span data-ttu-id="52b57-111">Abrufen von Zugriffstasten für einen bestimmten Signalisierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="52b57-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="52b57-112">Abrufen von Zugriffstasten aus einem Signalisierungs Dienstobjekt in Pipe</span><span class="sxs-lookup"><span data-stu-id="52b57-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="52b57-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="52b57-113">PARAMETERS</span></span>

### <span data-ttu-id="52b57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b57-114">-DefaultProfile</span></span>
<span data-ttu-id="52b57-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52b57-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b57-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="52b57-116">-InputObject</span></span>
<span data-ttu-id="52b57-117">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="52b57-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b57-118">-Name</span><span class="sxs-lookup"><span data-stu-id="52b57-118">-Name</span></span>
<span data-ttu-id="52b57-119">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="52b57-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b57-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b57-120">-ResourceGroupName</span></span>
<span data-ttu-id="52b57-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="52b57-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b57-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="52b57-122">-ResourceId</span></span>
<span data-ttu-id="52b57-123">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="52b57-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b57-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b57-124">CommonParameters</span></span>
<span data-ttu-id="52b57-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b57-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b57-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b57-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b57-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52b57-127">INPUTS</span></span>

### <span data-ttu-id="52b57-128">System. String</span><span class="sxs-lookup"><span data-stu-id="52b57-128">System.String</span></span>
<span data-ttu-id="52b57-129">Parameter: resourcecode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52b57-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="52b57-130">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="52b57-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="52b57-131">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52b57-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="52b57-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52b57-132">OUTPUTS</span></span>

### <span data-ttu-id="52b57-133">Microsoft. Azure. Commands. signalr. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="52b57-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="52b57-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="52b57-134">NOTES</span></span>

## <span data-ttu-id="52b57-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52b57-135">RELATED LINKS</span></span>
