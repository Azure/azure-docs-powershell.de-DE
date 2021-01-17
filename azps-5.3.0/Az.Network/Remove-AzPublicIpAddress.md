---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473448"
---
# <span data-ttu-id="8c60c-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c60c-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="8c60c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c60c-102">SYNOPSIS</span></span>
<span data-ttu-id="8c60c-103">Entfernt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8c60c-103">Removes a public IP address.</span></span>

## <span data-ttu-id="8c60c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c60c-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c60c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c60c-105">DESCRIPTION</span></span>
<span data-ttu-id="8c60c-106">Das **Cmdlet "Remove-AzPublicIpAddress"** entfernt eine öffentliche Azure-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8c60c-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="8c60c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c60c-107">EXAMPLES</span></span>

### <span data-ttu-id="8c60c-108">1: Entfernen einer öffentlichen IP-Adressressource</span><span class="sxs-lookup"><span data-stu-id="8c60c-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="8c60c-109">Mit diesem Befehl wird die öffentliche IP-Adressressource namens "$publicIpName in der Ressourcengruppe "$rgName.</span><span class="sxs-lookup"><span data-stu-id="8c60c-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="8c60c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c60c-110">PARAMETERS</span></span>

### <span data-ttu-id="8c60c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c60c-111">-AsJob</span></span>
<span data-ttu-id="8c60c-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8c60c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c60c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c60c-113">-DefaultProfile</span></span>
<span data-ttu-id="8c60c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c60c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c60c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8c60c-115">-Force</span></span>
<span data-ttu-id="8c60c-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="8c60c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c60c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8c60c-117">-Name</span></span>
<span data-ttu-id="8c60c-118">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8c60c-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c60c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c60c-119">-PassThru</span></span>
<span data-ttu-id="8c60c-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8c60c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c60c-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8c60c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c60c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c60c-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c60c-123">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8c60c-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c60c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c60c-124">-Confirm</span></span>
<span data-ttu-id="8c60c-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c60c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c60c-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8c60c-126">-WhatIf</span></span>
<span data-ttu-id="8c60c-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c60c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c60c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c60c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c60c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c60c-129">CommonParameters</span></span>
<span data-ttu-id="8c60c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c60c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c60c-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c60c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c60c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c60c-132">INPUTS</span></span>

### <span data-ttu-id="8c60c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8c60c-133">System.String</span></span>

## <span data-ttu-id="8c60c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c60c-134">OUTPUTS</span></span>

### <span data-ttu-id="8c60c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c60c-135">System.Boolean</span></span>

## <span data-ttu-id="8c60c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8c60c-136">NOTES</span></span>

## <span data-ttu-id="8c60c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8c60c-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c60c-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c60c-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="8c60c-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c60c-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="8c60c-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c60c-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


