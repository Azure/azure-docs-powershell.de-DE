---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476198"
---
# <span data-ttu-id="930f6-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="930f6-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="930f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="930f6-102">SYNOPSIS</span></span>
<span data-ttu-id="930f6-103">Erstellt ein IP-Tag-Objekt für eine Netzwerkschnittstelle eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="930f6-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="930f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="930f6-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="930f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="930f6-105">DESCRIPTION</span></span>
<span data-ttu-id="930f6-106">Das Cmdlet **New-AzureRmVmssIpTagConfig** erstellt ein IP-Tag-Konfigurationsobjekt für eine Netzwerkschnittstelle eines virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="930f6-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="930f6-107">Geben Sie die Konfiguration dieses Cmdlets als *IPTag* -Parameter des New-AzureRmVmssIpConfig-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="930f6-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="930f6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="930f6-108">EXAMPLES</span></span>

### <span data-ttu-id="930f6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="930f6-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="930f6-110">Dieser Befehl erstellt ein lokales IP-Tag-Objekt mit dem Typ "FirstPartyUsage" und "SQL" und erstellt dann eine IP-Konfiguration mit diesem IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="930f6-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="930f6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="930f6-111">PARAMETERS</span></span>

### <span data-ttu-id="930f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930f6-112">-DefaultProfile</span></span>
<span data-ttu-id="930f6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="930f6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="930f6-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="930f6-114">-IpTagType</span></span>
<span data-ttu-id="930f6-115">Gibt einen IP-Transpondertyp an.</span><span class="sxs-lookup"><span data-stu-id="930f6-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="930f6-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="930f6-116">-Tag</span></span>
<span data-ttu-id="930f6-117">Gibt einen IP-Transponderwert an.</span><span class="sxs-lookup"><span data-stu-id="930f6-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="930f6-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="930f6-118">-Confirm</span></span>
<span data-ttu-id="930f6-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="930f6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="930f6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="930f6-120">-WhatIf</span></span>
<span data-ttu-id="930f6-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="930f6-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="930f6-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="930f6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="930f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930f6-123">CommonParameters</span></span>
<span data-ttu-id="930f6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="930f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930f6-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="930f6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930f6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="930f6-126">INPUTS</span></span>

### <span data-ttu-id="930f6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="930f6-127">System.String</span></span>

## <span data-ttu-id="930f6-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="930f6-128">OUTPUTS</span></span>

### <span data-ttu-id="930f6-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="930f6-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="930f6-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="930f6-130">NOTES</span></span>

## <span data-ttu-id="930f6-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="930f6-131">RELATED LINKS</span></span>
