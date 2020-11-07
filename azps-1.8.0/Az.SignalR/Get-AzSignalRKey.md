---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: 72273a95447f9ab0b10460952bc4b26312b9efdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659303"
---
# <span data-ttu-id="7e20f-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="7e20f-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="7e20f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e20f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e20f-103">Rufen Sie die Zugriffstasten eines Signalisierungs Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="7e20f-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="7e20f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e20f-104">SYNTAX</span></span>

### <span data-ttu-id="7e20f-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e20f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e20f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e20f-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e20f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e20f-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e20f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e20f-108">DESCRIPTION</span></span>
<span data-ttu-id="7e20f-109">Rufen Sie die Zugriffstasten eines Signalisierungs Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="7e20f-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="7e20f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e20f-110">EXAMPLES</span></span>

### <span data-ttu-id="7e20f-111">Abrufen von Zugriffstasten für einen bestimmten Signalisierungs Dienst</span><span class="sxs-lookup"><span data-stu-id="7e20f-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="7e20f-112">Abrufen von Zugriffstasten aus einem Signalisierungs Dienstobjekt in Pipe</span><span class="sxs-lookup"><span data-stu-id="7e20f-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="7e20f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e20f-113">PARAMETERS</span></span>

### <span data-ttu-id="7e20f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e20f-114">-DefaultProfile</span></span>
<span data-ttu-id="7e20f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e20f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e20f-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7e20f-116">-InputObject</span></span>
<span data-ttu-id="7e20f-117">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="7e20f-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="7e20f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7e20f-118">-Name</span></span>
<span data-ttu-id="7e20f-119">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="7e20f-119">SignalR service name.</span></span>

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

### <span data-ttu-id="7e20f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e20f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7e20f-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e20f-121">Resource group name.</span></span>

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

### <span data-ttu-id="7e20f-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7e20f-122">-ResourceId</span></span>
<span data-ttu-id="7e20f-123">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="7e20f-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="7e20f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e20f-124">CommonParameters</span></span>
<span data-ttu-id="7e20f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e20f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e20f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e20f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e20f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e20f-127">INPUTS</span></span>

### <span data-ttu-id="7e20f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7e20f-128">System.String</span></span>

### <span data-ttu-id="7e20f-129">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7e20f-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="7e20f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e20f-130">OUTPUTS</span></span>

### <span data-ttu-id="7e20f-131">Microsoft. Azure. Commands. signalr. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="7e20f-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="7e20f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e20f-132">NOTES</span></span>

## <span data-ttu-id="7e20f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e20f-133">RELATED LINKS</span></span>
