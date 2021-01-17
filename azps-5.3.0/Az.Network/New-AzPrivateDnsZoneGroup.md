---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459916"
---
# <span data-ttu-id="4b797-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4b797-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4b797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b797-102">SYNOPSIS</span></span>
<span data-ttu-id="4b797-103">Erstellt eine private DNS-Zonengruppe im angegebenen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="4b797-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="4b797-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b797-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b797-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b797-105">DESCRIPTION</span></span>
<span data-ttu-id="4b797-106">Mit **dem Cmdlet "New-AzPrivateDnsZoneGroup"** können Sie eine neue private DNS-Zonengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b797-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="4b797-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b797-107">EXAMPLES</span></span>

### <span data-ttu-id="4b797-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b797-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="4b797-109">Nachdem der private Endpunkt erstellt wurde, erstellt das obige `test-pr-endpoint` Beispiel eine DNS-Zonengruppe unter diesem privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="4b797-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="4b797-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b797-110">PARAMETERS</span></span>

### <span data-ttu-id="4b797-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b797-111">-AsJob</span></span>
<span data-ttu-id="4b797-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4b797-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b797-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b797-113">-DefaultProfile</span></span>
<span data-ttu-id="4b797-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b797-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b797-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4b797-115">-Force</span></span>
<span data-ttu-id="4b797-116">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="4b797-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4b797-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4b797-117">-Name</span></span>
<span data-ttu-id="4b797-118">Der Name der privaten Dns-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b797-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="4b797-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="4b797-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="4b797-120">Eine Sammlung privater DNS-Zonenkonfigurationen der Gruppe der privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="4b797-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="4b797-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="4b797-121">-PrivateEndpointName</span></span>
<span data-ttu-id="4b797-122">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="4b797-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="4b797-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b797-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b797-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b797-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="4b797-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b797-125">-Confirm</span></span>
<span data-ttu-id="4b797-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b797-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b797-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4b797-127">-WhatIf</span></span>
<span data-ttu-id="4b797-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b797-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b797-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b797-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b797-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b797-130">CommonParameters</span></span>
<span data-ttu-id="4b797-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b797-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b797-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b797-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b797-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b797-133">INPUTS</span></span>

### <span data-ttu-id="4b797-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4b797-134">System.String</span></span>

### <span data-ttu-id="4b797-135">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4b797-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4b797-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b797-136">OUTPUTS</span></span>

### <span data-ttu-id="4b797-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4b797-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4b797-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b797-138">NOTES</span></span>

## <span data-ttu-id="4b797-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b797-139">RELATED LINKS</span></span>
