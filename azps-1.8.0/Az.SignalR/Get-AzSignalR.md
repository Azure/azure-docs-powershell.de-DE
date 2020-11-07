---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: be286c0a0006f1b8b054f32269bc06dc05bcf515
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659302"
---
# <span data-ttu-id="1da3b-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="1da3b-101">Get-AzSignalR</span></span>

## <span data-ttu-id="1da3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1da3b-102">SYNOPSIS</span></span>
<span data-ttu-id="1da3b-103">Besorgen Sie sich einen bestimmten Signalisierungs Dienst oder alle Signalisierungs Dienste in einer Ressourcengruppe oder einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1da3b-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="1da3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1da3b-104">SYNTAX</span></span>

### <span data-ttu-id="1da3b-105">ListSignalRServiceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1da3b-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1da3b-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1da3b-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1da3b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1da3b-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1da3b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1da3b-108">DESCRIPTION</span></span>
<span data-ttu-id="1da3b-109">Besorgen Sie sich einen bestimmten Signalisierungs Dienst oder alle Signalisierungs Dienste in einer Ressourcengruppe oder einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1da3b-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="1da3b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1da3b-110">EXAMPLES</span></span>

### <span data-ttu-id="1da3b-111">Abrufen aller Signalisierungs Dienste im Abonnement</span><span class="sxs-lookup"><span data-stu-id="1da3b-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="1da3b-112">Abrufen aller Signalisierungs Dienste in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1da3b-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="1da3b-113">Abrufen eines bestimmten Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="1da3b-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="1da3b-114">Abrufen eines bestimmten Signalisierungs Diensts aus der Standardressourcen Gruppe</span><span class="sxs-lookup"><span data-stu-id="1da3b-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="1da3b-115">Die Standardressourcen Gruppe kann durchgesetzt werden `Set-AzDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="1da3b-115">The default resource group can be set by `Set-AzDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="1da3b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="1da3b-116">PARAMETERS</span></span>

### <span data-ttu-id="1da3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da3b-117">-DefaultProfile</span></span>
<span data-ttu-id="1da3b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1da3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1da3b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1da3b-119">-Name</span></span>
<span data-ttu-id="1da3b-120">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="1da3b-120">SignalR service name.</span></span>

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

### <span data-ttu-id="1da3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="1da3b-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1da3b-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1da3b-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1da3b-123">-ResourceId</span></span>
<span data-ttu-id="1da3b-124">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="1da3b-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="1da3b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da3b-125">CommonParameters</span></span>
<span data-ttu-id="1da3b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da3b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da3b-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1da3b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da3b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1da3b-128">INPUTS</span></span>

### <span data-ttu-id="1da3b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1da3b-129">System.String</span></span>

## <span data-ttu-id="1da3b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1da3b-130">OUTPUTS</span></span>

### <span data-ttu-id="1da3b-131">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="1da3b-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="1da3b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1da3b-132">NOTES</span></span>

## <span data-ttu-id="1da3b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1da3b-133">RELATED LINKS</span></span>
