---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147460"
---
# <span data-ttu-id="e8987-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="e8987-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="e8987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8987-102">SYNOPSIS</span></span>
<span data-ttu-id="e8987-103">Generiert einen Schlüssel erneut, der für den Zugriff auf den REST-Endpunkt verwendet wird, der dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e8987-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="e8987-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8987-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8987-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8987-105">DESCRIPTION</span></span>
<span data-ttu-id="e8987-106">Das **Cmdlet Set-AzMediaServiceKey** generiert einen Schlüssel erneut, der für den Zugriff auf den Restendpunkt (Representational State Transfer) verwendet wird, der dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e8987-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="e8987-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8987-107">EXAMPLES</span></span>

### <span data-ttu-id="e8987-108">Beispiel 1: Erneutererieren des Primärschlüssels, der für den Zugriff auf den Mediendienst verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e8987-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="e8987-109">Mit diesem Befehl wird der Primärschlüssel für den Mediendienst mit dem Namen "MediaService001" erneut generiert, der zur Ressourcengruppe "ResourceGroup004" gehört.</span><span class="sxs-lookup"><span data-stu-id="e8987-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="e8987-110">Beispiel 2: Generiert den sekundären Schlüssel erneut, der für den Zugriff auf den Mediendienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8987-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="e8987-111">Mit diesem Befehl wird der sekundäre Schlüssel für den Mediendienst "MediaService002" erneut generiert, der zur Ressourcengruppe "Resourcegroup123" gehört.</span><span class="sxs-lookup"><span data-stu-id="e8987-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="e8987-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8987-112">PARAMETERS</span></span>

### <span data-ttu-id="e8987-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8987-113">-AccountName</span></span>
<span data-ttu-id="e8987-114">Gibt den Namen des Mediendiensts an, den dieses Cmdlet erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="e8987-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8987-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8987-115">-DefaultProfile</span></span>
<span data-ttu-id="e8987-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e8987-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8987-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e8987-117">-KeyType</span></span>
<span data-ttu-id="e8987-118">Gibt den Schlüsseltyp des Mediendiensts an.</span><span class="sxs-lookup"><span data-stu-id="e8987-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="e8987-119">Die zulässigen Werte für diesen Parameter sind: "Primary" oder "Secondary".</span><span class="sxs-lookup"><span data-stu-id="e8987-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8987-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8987-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8987-121">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="e8987-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="e8987-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8987-122">-Confirm</span></span>
<span data-ttu-id="e8987-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8987-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8987-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e8987-124">-WhatIf</span></span>
<span data-ttu-id="e8987-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8987-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8987-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8987-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8987-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8987-127">CommonParameters</span></span>
<span data-ttu-id="e8987-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8987-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8987-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8987-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8987-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8987-130">INPUTS</span></span>

### <span data-ttu-id="e8987-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e8987-131">System.String</span></span>

## <span data-ttu-id="e8987-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8987-132">OUTPUTS</span></span>

### <span data-ttu-id="e8987-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="e8987-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="e8987-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e8987-134">NOTES</span></span>

## <span data-ttu-id="e8987-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e8987-135">RELATED LINKS</span></span>

[<span data-ttu-id="e8987-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="e8987-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


