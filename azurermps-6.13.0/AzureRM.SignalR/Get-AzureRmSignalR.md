---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497286"
---
# <span data-ttu-id="2ff83-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="2ff83-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="2ff83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ff83-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff83-103">Besorgen Sie sich einen bestimmten Signalisierungs Dienst oder alle Signalisierungs Dienste in einer Ressourcengruppe oder einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ff83-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ff83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ff83-104">SYNTAX</span></span>

### <span data-ttu-id="2ff83-105">ListSignalRServiceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ff83-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ff83-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff83-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ff83-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff83-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ff83-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ff83-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff83-109">Besorgen Sie sich einen bestimmten Signalisierungs Dienst oder alle Signalisierungs Dienste in einer Ressourcengruppe oder einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ff83-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="2ff83-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ff83-110">EXAMPLES</span></span>

### <span data-ttu-id="2ff83-111">Abrufen aller Signalisierungs Dienste im Abonnement</span><span class="sxs-lookup"><span data-stu-id="2ff83-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="2ff83-112">Abrufen aller Signalisierungs Dienste in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2ff83-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="2ff83-113">Abrufen eines bestimmten Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="2ff83-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="2ff83-114">Abrufen eines bestimmten Signalisierungs Diensts aus der Standardressourcen Gruppe</span><span class="sxs-lookup"><span data-stu-id="2ff83-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="2ff83-115">Die Standardressourcen Gruppe kann durchgesetzt werden `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="2ff83-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="2ff83-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ff83-116">PARAMETERS</span></span>

### <span data-ttu-id="2ff83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff83-117">-DefaultProfile</span></span>
<span data-ttu-id="2ff83-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ff83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff83-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2ff83-119">-Name</span></span>
<span data-ttu-id="2ff83-120">Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="2ff83-120">SignalR service name.</span></span>

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

### <span data-ttu-id="2ff83-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff83-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ff83-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ff83-122">Resource group name.</span></span>

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

### <span data-ttu-id="2ff83-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2ff83-123">-ResourceId</span></span>
<span data-ttu-id="2ff83-124">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="2ff83-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="2ff83-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff83-125">CommonParameters</span></span>
<span data-ttu-id="2ff83-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff83-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff83-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff83-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff83-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ff83-128">INPUTS</span></span>

### <span data-ttu-id="2ff83-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2ff83-129">System.String</span></span>
<span data-ttu-id="2ff83-130">Parameter: resourcecode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ff83-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="2ff83-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ff83-131">OUTPUTS</span></span>

### <span data-ttu-id="2ff83-132">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="2ff83-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="2ff83-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ff83-133">NOTES</span></span>

## <span data-ttu-id="2ff83-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ff83-134">RELATED LINKS</span></span>
