---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: e4392b609081bb320e508de75319c9d50af12cae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660335"
---
# <span data-ttu-id="5df27-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5df27-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="5df27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5df27-102">SYNOPSIS</span></span>
<span data-ttu-id="5df27-103">Entfernt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5df27-103">Removes a public IP address.</span></span>

## <span data-ttu-id="5df27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df27-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df27-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5df27-105">DESCRIPTION</span></span>
<span data-ttu-id="5df27-106">Das Cmdlet **Remove-AzPublicIpAddress** entfernt eine Azure Public-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5df27-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="5df27-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5df27-107">EXAMPLES</span></span>

### <span data-ttu-id="5df27-108">1: Entfernen einer öffentlichen IP-Adressen Ressource</span><span class="sxs-lookup"><span data-stu-id="5df27-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="5df27-109">Dieser Befehl entfernt die öffentliche IP-Adressen Ressource mit dem Namen $publicIpName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="5df27-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="5df27-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5df27-110">PARAMETERS</span></span>

### <span data-ttu-id="5df27-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5df27-111">-AsJob</span></span>
<span data-ttu-id="5df27-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5df27-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5df27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df27-113">-DefaultProfile</span></span>
<span data-ttu-id="5df27-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5df27-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5df27-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5df27-115">-Force</span></span>
<span data-ttu-id="5df27-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5df27-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5df27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5df27-117">-Name</span></span>
<span data-ttu-id="5df27-118">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5df27-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5df27-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5df27-119">-PassThru</span></span>
<span data-ttu-id="5df27-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5df27-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5df27-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5df27-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5df27-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df27-122">-ResourceGroupName</span></span>
<span data-ttu-id="5df27-123">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5df27-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5df27-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5df27-124">-Confirm</span></span>
<span data-ttu-id="5df27-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5df27-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df27-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df27-126">-WhatIf</span></span>
<span data-ttu-id="5df27-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5df27-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df27-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5df27-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df27-129">CommonParameters</span></span>
<span data-ttu-id="5df27-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df27-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df27-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df27-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5df27-132">INPUTS</span></span>

### <span data-ttu-id="5df27-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5df27-133">System.String</span></span>

## <span data-ttu-id="5df27-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5df27-134">OUTPUTS</span></span>

### <span data-ttu-id="5df27-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5df27-135">System.Boolean</span></span>

## <span data-ttu-id="5df27-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5df27-136">NOTES</span></span>

## <span data-ttu-id="5df27-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5df27-137">RELATED LINKS</span></span>

[<span data-ttu-id="5df27-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5df27-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="5df27-139">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5df27-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="5df27-140">Satz-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5df27-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


