---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 396f603c4a4126b8d438f0048677da7a5dbd7492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497053"
---
# <span data-ttu-id="c0244-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0244-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="c0244-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0244-102">SYNOPSIS</span></span>
<span data-ttu-id="c0244-103">Entfernt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c0244-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0244-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0244-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0244-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0244-105">DESCRIPTION</span></span>
<span data-ttu-id="c0244-106">Das Cmdlet **Remove-AzureRmPublicIpAddress** entfernt eine Azure Public-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c0244-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="c0244-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0244-107">EXAMPLES</span></span>

### <span data-ttu-id="c0244-108">1: Entfernen einer öffentlichen IP-Adressen Ressource</span><span class="sxs-lookup"><span data-stu-id="c0244-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c0244-109">Dieser Befehl entfernt die öffentliche IP-Adressen Ressource mit dem Namen $publicIpName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="c0244-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="c0244-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0244-110">PARAMETERS</span></span>

### <span data-ttu-id="c0244-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c0244-111">-Force</span></span>
<span data-ttu-id="c0244-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c0244-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0244-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c0244-113">-Name</span></span>
<span data-ttu-id="c0244-114">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c0244-114">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c0244-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0244-115">-PassThru</span></span>
<span data-ttu-id="c0244-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c0244-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0244-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c0244-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0244-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0244-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0244-119">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c0244-119">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c0244-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0244-120">-Confirm</span></span>
<span data-ttu-id="c0244-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0244-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0244-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0244-122">-WhatIf</span></span>
<span data-ttu-id="c0244-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0244-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0244-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0244-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0244-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0244-125">-DefaultProfile</span></span>
<span data-ttu-id="c0244-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0244-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0244-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0244-127">CommonParameters</span></span>
<span data-ttu-id="c0244-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0244-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0244-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0244-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0244-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0244-130">INPUTS</span></span>

## <span data-ttu-id="c0244-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0244-131">OUTPUTS</span></span>

## <span data-ttu-id="c0244-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0244-132">NOTES</span></span>

## <span data-ttu-id="c0244-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0244-133">RELATED LINKS</span></span>

[<span data-ttu-id="c0244-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0244-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c0244-135">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0244-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c0244-136">Satz-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c0244-136">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


