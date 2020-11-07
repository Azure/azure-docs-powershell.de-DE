---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: af8a85c698a59a31516c6dee05bb57415a45ff62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849100"
---
# <span data-ttu-id="b2e84-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b2e84-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="b2e84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2e84-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e84-103">Entfernt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b2e84-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2e84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2e84-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e84-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2e84-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e84-106">Das Cmdlet **Remove-AzureRmPublicIpAddress** entfernt eine Azure Public-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b2e84-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="b2e84-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2e84-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e84-108">1: Entfernen einer öffentlichen IP-Adressen Ressource</span><span class="sxs-lookup"><span data-stu-id="b2e84-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="b2e84-109">Dieser Befehl entfernt die öffentliche IP-Adressen Ressource mit dem Namen $publicIpName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="b2e84-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="b2e84-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e84-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e84-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2e84-111">-AsJob</span></span>
<span data-ttu-id="b2e84-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b2e84-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2e84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e84-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e84-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2e84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e84-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b2e84-115">-Force</span></span>
<span data-ttu-id="b2e84-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b2e84-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2e84-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2e84-117">-Name</span></span>
<span data-ttu-id="b2e84-118">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b2e84-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e84-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2e84-119">-PassThru</span></span>
<span data-ttu-id="b2e84-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b2e84-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b2e84-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b2e84-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2e84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e84-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2e84-123">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b2e84-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e84-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2e84-124">-Confirm</span></span>
<span data-ttu-id="b2e84-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2e84-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e84-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e84-126">-WhatIf</span></span>
<span data-ttu-id="b2e84-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2e84-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e84-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2e84-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e84-129">CommonParameters</span></span>
<span data-ttu-id="b2e84-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e84-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e84-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e84-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2e84-132">INPUTS</span></span>

## <span data-ttu-id="b2e84-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2e84-133">OUTPUTS</span></span>

## <span data-ttu-id="b2e84-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2e84-134">NOTES</span></span>

## <span data-ttu-id="b2e84-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2e84-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2e84-136">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b2e84-136">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="b2e84-137">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b2e84-137">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="b2e84-138">Satz-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b2e84-138">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


