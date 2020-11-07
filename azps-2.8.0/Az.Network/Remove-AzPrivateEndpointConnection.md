---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822839"
---
# <span data-ttu-id="28027-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="28027-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="28027-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28027-102">SYNOPSIS</span></span>
<span data-ttu-id="28027-103">Entfernt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="28027-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="28027-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28027-104">SYNTAX</span></span>

### <span data-ttu-id="28027-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="28027-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28027-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="28027-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28027-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28027-107">DESCRIPTION</span></span>
<span data-ttu-id="28027-108">Das Cmdlet " **Remove-AzPrivateEndpointConnection** " entfernt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="28027-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="28027-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28027-109">EXAMPLES</span></span>

### <span data-ttu-id="28027-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28027-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="28027-111">In diesem Beispiel wird eine private Endpunkt Verbindung mit dem Namen MyPrivateEndpointConnection1 entfernt</span><span class="sxs-lookup"><span data-stu-id="28027-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="28027-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="28027-112">PARAMETERS</span></span>

### <span data-ttu-id="28027-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28027-113">-AsJob</span></span>
<span data-ttu-id="28027-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="28027-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28027-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28027-115">-DefaultProfile</span></span>
<span data-ttu-id="28027-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28027-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28027-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28027-117">-Description</span></span>
<span data-ttu-id="28027-118">Der Grund für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="28027-118">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28027-119">-Force</span><span class="sxs-lookup"><span data-stu-id="28027-119">-Force</span></span>
<span data-ttu-id="28027-120">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="28027-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="28027-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28027-121">-Name</span></span>
<span data-ttu-id="28027-122">Der Name der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="28027-122">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28027-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28027-123">-PassThru</span></span>
<span data-ttu-id="28027-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="28027-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28027-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="28027-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28027-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28027-126">-ResourceGroupName</span></span>
<span data-ttu-id="28027-127">Der Ressourcengruppenname der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="28027-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28027-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="28027-128">-ResourceId</span></span>
<span data-ttu-id="28027-129">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="28027-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28027-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28027-130">-ServiceName</span></span>
<span data-ttu-id="28027-131">Der Name des privaten Link Diensts mit der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="28027-131">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28027-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28027-132">-Confirm</span></span>
<span data-ttu-id="28027-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28027-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28027-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28027-134">-WhatIf</span></span>
<span data-ttu-id="28027-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28027-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28027-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28027-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28027-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28027-137">CommonParameters</span></span>
<span data-ttu-id="28027-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28027-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28027-139">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28027-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28027-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28027-140">INPUTS</span></span>

### <span data-ttu-id="28027-141">System. String</span><span class="sxs-lookup"><span data-stu-id="28027-141">System.String</span></span>

## <span data-ttu-id="28027-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28027-142">OUTPUTS</span></span>

### <span data-ttu-id="28027-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28027-143">System.Boolean</span></span>

## <span data-ttu-id="28027-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="28027-144">NOTES</span></span>

## <span data-ttu-id="28027-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28027-145">RELATED LINKS</span></span>

[<span data-ttu-id="28027-146">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="28027-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
