---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946240"
---
# <span data-ttu-id="e2e41-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="e2e41-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="e2e41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e41-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e41-103">Erstellt ein IP-Tag-Objekt für eine Netzwerkschnittstelle eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2e41-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="e2e41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2e41-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e41-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2e41-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e41-106">Das **Cmdlet New-AzVmssIpTagConfig** erstellt ein IP-Tag-Konfigurationsobjekt für eine Netzwerkschnittstelle eines VmSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="e2e41-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e2e41-107">Geben Sie die Konfiguration aus diesem Cmdlet als *New-AzVmssIpConfig* des New-AzVmssIpConfig an.</span><span class="sxs-lookup"><span data-stu-id="e2e41-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="e2e41-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2e41-108">EXAMPLES</span></span>

### <span data-ttu-id="e2e41-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2e41-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="e2e41-110">Mit diesem Befehl wird ein lokales IP-Tag-Objekt mit dem Typ "FirstPartyUsage" und dem Tag "Sql" erstellt und dann eine IP-Konfiguration mit diesem IP-Tag erstellt.</span><span class="sxs-lookup"><span data-stu-id="e2e41-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="e2e41-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e2e41-111">PARAMETERS</span></span>

### <span data-ttu-id="e2e41-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e41-112">-DefaultProfile</span></span>
<span data-ttu-id="e2e41-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2e41-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e41-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="e2e41-114">-IpTagType</span></span>
<span data-ttu-id="e2e41-115">Gibt einen IP-Tag-Typ an.</span><span class="sxs-lookup"><span data-stu-id="e2e41-115">Specifies an IP Tag Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e41-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2e41-116">-Tag</span></span>
<span data-ttu-id="e2e41-117">Gibt einen IP-Tag-Wert an.</span><span class="sxs-lookup"><span data-stu-id="e2e41-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="e2e41-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e2e41-118">-Confirm</span></span>
<span data-ttu-id="e2e41-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2e41-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2e41-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e41-120">-WhatIf</span></span>
<span data-ttu-id="e2e41-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2e41-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2e41-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2e41-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2e41-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e41-123">CommonParameters</span></span>
<span data-ttu-id="e2e41-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e41-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e41-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2e41-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e41-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2e41-126">INPUTS</span></span>

### <span data-ttu-id="e2e41-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e2e41-127">System.String</span></span>

## <span data-ttu-id="e2e41-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2e41-128">OUTPUTS</span></span>

### <span data-ttu-id="e2e41-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="e2e41-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="e2e41-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e2e41-130">NOTES</span></span>

## <span data-ttu-id="e2e41-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e2e41-131">RELATED LINKS</span></span>
