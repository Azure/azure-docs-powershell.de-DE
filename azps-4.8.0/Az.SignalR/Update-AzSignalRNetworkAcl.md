---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010470"
---
# <span data-ttu-id="e3ece-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="e3ece-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="e3ece-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3ece-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ece-103">Aktualisieren Sie die Netzwerk-ACL eines Signalisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="e3ece-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="e3ece-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3ece-104">SYNTAX</span></span>

### <span data-ttu-id="e3ece-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3ece-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3ece-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3ece-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3ece-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3ece-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3ece-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3ece-108">DESCRIPTION</span></span>
<span data-ttu-id="e3ece-109">Aktualisieren Sie die Netzwerk-ACL eines Signalisierungs Diensts, einschließlich der Standardaktion und der Netzwerk-ACLs für öffentliche und private Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="e3ece-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="e3ece-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3ece-110">EXAMPLES</span></span>

### <span data-ttu-id="e3ece-111">Zulassen von RESTAPI, ClientConnection für öffentliches Netzwerk und Festlegen der Standardaktion für "verweigern"</span><span class="sxs-lookup"><span data-stu-id="e3ece-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="e3ece-112">Clientverbindung und Serververbindung für eine private Endpunkt Verbindung zulassen</span><span class="sxs-lookup"><span data-stu-id="e3ece-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="e3ece-113">Verweigern der Clientverbindung für öffentliches Netzwerk und eine private Endpunkt Verbindung</span><span class="sxs-lookup"><span data-stu-id="e3ece-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="e3ece-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3ece-114">PARAMETERS</span></span>

### <span data-ttu-id="e3ece-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="e3ece-115">-Allow</span></span>
<span data-ttu-id="e3ece-116">Zulässige Netzwerk-ACLs</span><span class="sxs-lookup"><span data-stu-id="e3ece-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3ece-117">-AsJob</span></span>
<span data-ttu-id="e3ece-118">Führen Sie das Cmdlet im Hintergrund Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="e3ece-118">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-119">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="e3ece-119">-DefaultAction</span></span>
<span data-ttu-id="e3ece-120">Standardaktion der Signalisierungs-Netzwerk-ACLs, entweder Allow oder Deny.</span><span class="sxs-lookup"><span data-stu-id="e3ece-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="e3ece-121">Sie entscheidet, ob die Option Netzwerk-ACLs ablehnen oder Netzwerk-ACLs zulassen wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="e3ece-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="e3ece-122">Wenn beispielsweise die Standardaktion Allow ist, sind nur die Deny-ACLs wichtig.</span><span class="sxs-lookup"><span data-stu-id="e3ece-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ece-123">-DefaultProfile</span></span>
<span data-ttu-id="e3ece-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3ece-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ece-125">-Ablehnen</span><span class="sxs-lookup"><span data-stu-id="e3ece-125">-Deny</span></span>
<span data-ttu-id="e3ece-126">Verweigerte Netzwerk-ACLs</span><span class="sxs-lookup"><span data-stu-id="e3ece-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e3ece-127">-InputObject</span></span>
<span data-ttu-id="e3ece-128">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="e3ece-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="e3ece-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e3ece-129">-Name</span></span>
<span data-ttu-id="e3ece-130">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="e3ece-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="e3ece-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="e3ece-131">-PrivateEndpointName</span></span>
<span data-ttu-id="e3ece-132">Name (n) privater Endpunkt (e), die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="e3ece-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="e3ece-133">-PublicNetwork</span></span>
<span data-ttu-id="e3ece-134">Aktualisieren von ACLs für öffentliche Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e3ece-134">Update public network ACLs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ece-135">-ResourceGroupName</span></span>
<span data-ttu-id="e3ece-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3ece-136">The resource group name.</span></span>
<span data-ttu-id="e3ece-137">Wenn nicht angegeben, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3ece-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="e3ece-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e3ece-138">-ResourceId</span></span>
<span data-ttu-id="e3ece-139">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="e3ece-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3ece-140">-Confirm</span></span>
<span data-ttu-id="e3ece-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3ece-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ece-142">-WhatIf</span></span>
<span data-ttu-id="e3ece-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3ece-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ece-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3ece-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ece-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ece-145">CommonParameters</span></span>
<span data-ttu-id="e3ece-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ece-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ece-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3ece-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ece-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3ece-148">INPUTS</span></span>

### <span data-ttu-id="e3ece-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e3ece-149">System.String</span></span>

## <span data-ttu-id="e3ece-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3ece-150">OUTPUTS</span></span>

### <span data-ttu-id="e3ece-151">Microsoft. Azure. Commands. signalr. Models. PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="e3ece-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="e3ece-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3ece-152">NOTES</span></span>

## <span data-ttu-id="e3ece-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3ece-153">RELATED LINKS</span></span>
