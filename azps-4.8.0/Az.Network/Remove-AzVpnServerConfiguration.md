---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173188"
---
# <span data-ttu-id="7bcea-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bcea-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="7bcea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bcea-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcea-103">Entfernt eine vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7bcea-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="7bcea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bcea-104">SYNTAX</span></span>

### <span data-ttu-id="7bcea-105">ByVpnServerConfigurationName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bcea-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcea-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="7bcea-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcea-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="7bcea-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bcea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bcea-108">DESCRIPTION</span></span>
<span data-ttu-id="7bcea-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="7bcea-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7bcea-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bcea-110">EXAMPLES</span></span>

### <span data-ttu-id="7bcea-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bcea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="7bcea-112">Der obige Befehl entfernt eine vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7bcea-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="7bcea-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bcea-113">PARAMETERS</span></span>

### <span data-ttu-id="7bcea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcea-114">-DefaultProfile</span></span>
<span data-ttu-id="7bcea-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bcea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7bcea-116">-Force</span></span>
<span data-ttu-id="7bcea-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="7bcea-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7bcea-118">-InputObject</span></span>
<span data-ttu-id="7bcea-119">Das vpnServerConfiguration-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bcea-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7bcea-120">-Name</span></span>
<span data-ttu-id="7bcea-121">Der vpnServerConfiguration-Name.</span><span class="sxs-lookup"><span data-stu-id="7bcea-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bcea-122">-PassThru</span></span>
<span data-ttu-id="7bcea-123">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bcea-123">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bcea-124">-ResourceGroupName</span></span>
<span data-ttu-id="7bcea-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7bcea-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7bcea-126">-ResourceId</span></span>
<span data-ttu-id="7bcea-127">Die Azure-Ressourcen-ID für die vpnServerConfiguration, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bcea-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bcea-128">-Confirm</span></span>
<span data-ttu-id="7bcea-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bcea-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bcea-130">-WhatIf</span></span>
<span data-ttu-id="7bcea-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bcea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bcea-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bcea-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcea-133">CommonParameters</span></span>
<span data-ttu-id="7bcea-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bcea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcea-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bcea-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcea-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bcea-136">INPUTS</span></span>

### <span data-ttu-id="7bcea-137">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bcea-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="7bcea-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7bcea-138">System.String</span></span>

## <span data-ttu-id="7bcea-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bcea-139">OUTPUTS</span></span>

### <span data-ttu-id="7bcea-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7bcea-140">System.Boolean</span></span>

## <span data-ttu-id="7bcea-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bcea-141">NOTES</span></span>

## <span data-ttu-id="7bcea-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bcea-142">RELATED LINKS</span></span>
