---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364046"
---
# <span data-ttu-id="af582-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="af582-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="af582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af582-102">SYNOPSIS</span></span>
<span data-ttu-id="af582-103">Aktualisierungen der GRUPPE "DNS-Zone"</span><span class="sxs-lookup"><span data-stu-id="af582-103">Updates DNS zone group</span></span>

## <span data-ttu-id="af582-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af582-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af582-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af582-105">DESCRIPTION</span></span>
<span data-ttu-id="af582-106">Das **Cmdlet "Set-AzPrivateDnsZoneGroup"** aktualisiert die DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="af582-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="af582-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af582-107">EXAMPLES</span></span>

### <span data-ttu-id="af582-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af582-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="af582-109">Im obigen Beispiel wird die DNS-Zonengruppe "dnsgroup1" mit einer neuen Dnsconfig aktualisiert, die mit einer anderen DNS-Zone verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="af582-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="af582-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af582-110">PARAMETERS</span></span>

### <span data-ttu-id="af582-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af582-111">-AsJob</span></span>
<span data-ttu-id="af582-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="af582-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af582-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af582-113">-DefaultProfile</span></span>
<span data-ttu-id="af582-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af582-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af582-115">-Name</span><span class="sxs-lookup"><span data-stu-id="af582-115">-Name</span></span>
<span data-ttu-id="af582-116">Der Name der privaten Dns-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="af582-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af582-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="af582-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="af582-118">Eine Sammlung privater DNS-Zonenkonfigurationen der Gruppe der privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="af582-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af582-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="af582-119">-PrivateEndpointName</span></span>
<span data-ttu-id="af582-120">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="af582-120">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af582-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af582-121">-ResourceGroupName</span></span>
<span data-ttu-id="af582-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="af582-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af582-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af582-123">-Confirm</span></span>
<span data-ttu-id="af582-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af582-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af582-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="af582-125">-WhatIf</span></span>
<span data-ttu-id="af582-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af582-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af582-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af582-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af582-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af582-128">CommonParameters</span></span>
<span data-ttu-id="af582-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af582-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af582-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af582-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af582-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af582-131">INPUTS</span></span>

### <span data-ttu-id="af582-132">System.String</span><span class="sxs-lookup"><span data-stu-id="af582-132">System.String</span></span>

### <span data-ttu-id="af582-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="af582-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="af582-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af582-134">OUTPUTS</span></span>

### <span data-ttu-id="af582-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="af582-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="af582-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af582-136">NOTES</span></span>

## <span data-ttu-id="af582-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af582-137">RELATED LINKS</span></span>
