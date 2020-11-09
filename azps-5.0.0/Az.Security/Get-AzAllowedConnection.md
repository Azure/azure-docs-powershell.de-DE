---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300945"
---
# <span data-ttu-id="cfc89-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="cfc89-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="cfc89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfc89-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc89-103">Wird verwendet, um den zulässigen Datenverkehr zwischen den Ressourcen für das Abonnement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cfc89-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="cfc89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfc89-104">SYNTAX</span></span>

### <span data-ttu-id="cfc89-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfc89-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfc89-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="cfc89-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfc89-107">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cfc89-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfc89-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfc89-108">DESCRIPTION</span></span>
<span data-ttu-id="cfc89-109">Ruft die Liste aller möglichen Datenverkehr zwischen Ressourcen für das Abonnement und den Speicherort auf Grundlage des Verbindungstyps ab.</span><span class="sxs-lookup"><span data-stu-id="cfc89-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="cfc89-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfc89-110">EXAMPLES</span></span>

### <span data-ttu-id="cfc89-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfc89-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="cfc89-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cfc89-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="cfc89-113">Ruft die Liste aller möglichen Datenverkehr zwischen Ressourcen für das Abonnement und den Speicherort auf Grundlage des Verbindungstyps ab.</span><span class="sxs-lookup"><span data-stu-id="cfc89-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="cfc89-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfc89-114">PARAMETERS</span></span>

### <span data-ttu-id="cfc89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc89-115">-DefaultProfile</span></span>
<span data-ttu-id="cfc89-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfc89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc89-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="cfc89-117">-Location</span></span>
<span data-ttu-id="cfc89-118">Lage.</span><span class="sxs-lookup"><span data-stu-id="cfc89-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cfc89-119">-Name</span></span>
<span data-ttu-id="cfc89-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="cfc89-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfc89-121">-ResourceGroupName</span></span>
<span data-ttu-id="cfc89-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cfc89-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cfc89-123">-ResourceId</span></span>
<span data-ttu-id="cfc89-124">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="cfc89-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc89-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc89-125">CommonParameters</span></span>
<span data-ttu-id="cfc89-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc89-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc89-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc89-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc89-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfc89-128">INPUTS</span></span>

### <span data-ttu-id="cfc89-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc89-129">System.String</span></span>

## <span data-ttu-id="cfc89-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfc89-130">OUTPUTS</span></span>

### <span data-ttu-id="cfc89-131">Microsoft. Azure. Commands. Security. Models. AllowedConnection. PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="cfc89-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="cfc89-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfc89-132">NOTES</span></span>

## <span data-ttu-id="cfc89-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfc89-133">RELATED LINKS</span></span>
