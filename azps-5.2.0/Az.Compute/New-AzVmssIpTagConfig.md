---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297840"
---
# <span data-ttu-id="142bc-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="142bc-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="142bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="142bc-102">SYNOPSIS</span></span>
<span data-ttu-id="142bc-103">Erstellt ein IP-Tag-Objekt für eine Netzwerkschnittstelle einer VMSS.</span><span class="sxs-lookup"><span data-stu-id="142bc-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="142bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="142bc-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="142bc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="142bc-105">DESCRIPTION</span></span>
<span data-ttu-id="142bc-106">Das **Cmdlet "New-AzVmssIpTagConfig"** erstellt ein #A0 für eine Netzwerkschnittstelle eines Virtual Machine Scale Set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="142bc-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="142bc-107">Geben Sie die Konfiguration dieses  Cmdlets als New-AzVmssIpConfig des New-AzVmssIpConfig an.</span><span class="sxs-lookup"><span data-stu-id="142bc-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="142bc-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="142bc-108">EXAMPLES</span></span>

### <span data-ttu-id="142bc-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="142bc-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="142bc-110">Dieser Befehl erstellt ein lokales IP-Tag-Objekt mit dem Typ "FirstPartyUsage" und dem Tag "Sql" und erstellt dann eine IP-Konfiguration mit diesem IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="142bc-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="142bc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="142bc-111">PARAMETERS</span></span>

### <span data-ttu-id="142bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="142bc-112">-DefaultProfile</span></span>
<span data-ttu-id="142bc-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="142bc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="142bc-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="142bc-114">-IpTagType</span></span>
<span data-ttu-id="142bc-115">Gibt einen IP-Tag-Typ an.</span><span class="sxs-lookup"><span data-stu-id="142bc-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="142bc-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="142bc-116">-Tag</span></span>
<span data-ttu-id="142bc-117">Gibt einen Wert für ein IP-Tag an.</span><span class="sxs-lookup"><span data-stu-id="142bc-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="142bc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="142bc-118">-Confirm</span></span>
<span data-ttu-id="142bc-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="142bc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="142bc-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="142bc-120">-WhatIf</span></span>
<span data-ttu-id="142bc-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="142bc-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="142bc-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="142bc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="142bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142bc-123">CommonParameters</span></span>
<span data-ttu-id="142bc-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="142bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142bc-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="142bc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142bc-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="142bc-126">INPUTS</span></span>

### <span data-ttu-id="142bc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="142bc-127">System.String</span></span>

## <span data-ttu-id="142bc-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="142bc-128">OUTPUTS</span></span>

### <span data-ttu-id="142bc-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="142bc-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="142bc-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="142bc-130">NOTES</span></span>

## <span data-ttu-id="142bc-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="142bc-131">RELATED LINKS</span></span>
