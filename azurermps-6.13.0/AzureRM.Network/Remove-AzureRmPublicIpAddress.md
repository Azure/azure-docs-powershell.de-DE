---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 6d294bd4b6f016ed1731a71528b39adc3bbe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503518"
---
# <span data-ttu-id="66932-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66932-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="66932-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66932-102">SYNOPSIS</span></span>
<span data-ttu-id="66932-103">Entfernt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="66932-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66932-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66932-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66932-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66932-105">DESCRIPTION</span></span>
<span data-ttu-id="66932-106">Das Cmdlet **Remove-AzureRmPublicIpAddress** entfernt eine Azure Public-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="66932-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="66932-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66932-107">EXAMPLES</span></span>

### <span data-ttu-id="66932-108">1: Entfernen einer öffentlichen IP-Adressen Ressource</span><span class="sxs-lookup"><span data-stu-id="66932-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="66932-109">Dieser Befehl entfernt die öffentliche IP-Adressen Ressource mit dem Namen $publicIpName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="66932-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="66932-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66932-110">PARAMETERS</span></span>

### <span data-ttu-id="66932-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66932-111">-AsJob</span></span>
<span data-ttu-id="66932-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="66932-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66932-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66932-113">-DefaultProfile</span></span>
<span data-ttu-id="66932-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66932-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66932-115">-Force</span><span class="sxs-lookup"><span data-stu-id="66932-115">-Force</span></span>
<span data-ttu-id="66932-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="66932-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66932-117">-Name</span><span class="sxs-lookup"><span data-stu-id="66932-117">-Name</span></span>
<span data-ttu-id="66932-118">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="66932-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66932-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66932-119">-PassThru</span></span>
<span data-ttu-id="66932-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="66932-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66932-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="66932-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66932-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66932-122">-ResourceGroupName</span></span>
<span data-ttu-id="66932-123">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="66932-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66932-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66932-124">-Confirm</span></span>
<span data-ttu-id="66932-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66932-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66932-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66932-126">-WhatIf</span></span>
<span data-ttu-id="66932-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66932-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66932-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66932-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66932-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66932-129">CommonParameters</span></span>
<span data-ttu-id="66932-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66932-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66932-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66932-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66932-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66932-132">INPUTS</span></span>

### <span data-ttu-id="66932-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66932-133">System.String</span></span>

## <span data-ttu-id="66932-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66932-134">OUTPUTS</span></span>

### <span data-ttu-id="66932-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66932-135">System.Boolean</span></span>

## <span data-ttu-id="66932-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="66932-136">NOTES</span></span>

## <span data-ttu-id="66932-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66932-137">RELATED LINKS</span></span>

[<span data-ttu-id="66932-138">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66932-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="66932-139">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66932-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="66932-140">Satz-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="66932-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


