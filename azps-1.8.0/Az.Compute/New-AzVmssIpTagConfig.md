---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: ee85085f27b7d4b94753b40edc8f6a24630c88d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661502"
---
# <span data-ttu-id="4236a-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="4236a-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="4236a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4236a-102">SYNOPSIS</span></span>
<span data-ttu-id="4236a-103">Erstellt ein IP-Tag-Objekt für eine Netzwerkschnittstelle eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="4236a-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="4236a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4236a-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4236a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4236a-105">DESCRIPTION</span></span>
<span data-ttu-id="4236a-106">Das Cmdlet **New-AzVmssIpTagConfig** erstellt ein IP-Tag-Konfigurationsobjekt für eine Netzwerkschnittstelle eines virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4236a-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="4236a-107">Geben Sie die Konfiguration dieses Cmdlets als *IPTag* -Parameter des New-AzVmssIpConfig-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="4236a-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="4236a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4236a-108">EXAMPLES</span></span>

### <span data-ttu-id="4236a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4236a-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="4236a-110">Dieser Befehl erstellt ein lokales IP-Tag-Objekt mit dem Typ "FirstPartyUsage" und "SQL" und erstellt dann eine IP-Konfiguration mit diesem IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="4236a-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="4236a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4236a-111">PARAMETERS</span></span>

### <span data-ttu-id="4236a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4236a-112">-DefaultProfile</span></span>
<span data-ttu-id="4236a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4236a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4236a-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="4236a-114">-IpTagType</span></span>
<span data-ttu-id="4236a-115">Gibt einen IP-Transpondertyp an.</span><span class="sxs-lookup"><span data-stu-id="4236a-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="4236a-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="4236a-116">-Tag</span></span>
<span data-ttu-id="4236a-117">Gibt einen IP-Transponderwert an.</span><span class="sxs-lookup"><span data-stu-id="4236a-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="4236a-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4236a-118">-Confirm</span></span>
<span data-ttu-id="4236a-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4236a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4236a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4236a-120">-WhatIf</span></span>
<span data-ttu-id="4236a-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4236a-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4236a-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4236a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4236a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4236a-123">CommonParameters</span></span>
<span data-ttu-id="4236a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4236a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4236a-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4236a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4236a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4236a-126">INPUTS</span></span>

### <span data-ttu-id="4236a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4236a-127">System.String</span></span>

## <span data-ttu-id="4236a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4236a-128">OUTPUTS</span></span>

### <span data-ttu-id="4236a-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="4236a-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="4236a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4236a-130">NOTES</span></span>

## <span data-ttu-id="4236a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4236a-131">RELATED LINKS</span></span>
