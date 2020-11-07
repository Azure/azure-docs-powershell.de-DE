---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 299e27d0d4824dfe06a6f1982f4eda1a04eeb1c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843779"
---
# <span data-ttu-id="c265b-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c265b-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="c265b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c265b-102">SYNOPSIS</span></span>
<span data-ttu-id="c265b-103">Entfernt eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c265b-103">Removes a public IP address.</span></span>

## <span data-ttu-id="c265b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c265b-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c265b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c265b-105">DESCRIPTION</span></span>
<span data-ttu-id="c265b-106">Das Cmdlet **Remove-AzPublicIpAddress** entfernt eine Azure Public-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c265b-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="c265b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c265b-107">EXAMPLES</span></span>

### <span data-ttu-id="c265b-108">1: Entfernen einer öffentlichen IP-Adressen Ressource</span><span class="sxs-lookup"><span data-stu-id="c265b-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c265b-109">Dieser Befehl entfernt die öffentliche IP-Adressen Ressource mit dem Namen $publicIpName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="c265b-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="c265b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c265b-110">PARAMETERS</span></span>

### <span data-ttu-id="c265b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c265b-111">-AsJob</span></span>
<span data-ttu-id="c265b-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c265b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c265b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c265b-113">-DefaultProfile</span></span>
<span data-ttu-id="c265b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c265b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c265b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c265b-115">-Force</span></span>
<span data-ttu-id="c265b-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c265b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c265b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c265b-117">-Name</span></span>
<span data-ttu-id="c265b-118">Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c265b-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c265b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c265b-119">-PassThru</span></span>
<span data-ttu-id="c265b-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c265b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c265b-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c265b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c265b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c265b-122">-ResourceGroupName</span></span>
<span data-ttu-id="c265b-123">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c265b-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c265b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c265b-124">-Confirm</span></span>
<span data-ttu-id="c265b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c265b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c265b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c265b-126">-WhatIf</span></span>
<span data-ttu-id="c265b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c265b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c265b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c265b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c265b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c265b-129">CommonParameters</span></span>
<span data-ttu-id="c265b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c265b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c265b-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c265b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c265b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c265b-132">INPUTS</span></span>

## <span data-ttu-id="c265b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c265b-133">OUTPUTS</span></span>

## <span data-ttu-id="c265b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c265b-134">NOTES</span></span>

## <span data-ttu-id="c265b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c265b-135">RELATED LINKS</span></span>

[<span data-ttu-id="c265b-136">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c265b-136">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="c265b-137">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c265b-137">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="c265b-138">Satz-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c265b-138">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


