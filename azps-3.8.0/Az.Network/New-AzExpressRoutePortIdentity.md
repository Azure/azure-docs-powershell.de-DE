---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996363"
---
# <span data-ttu-id="196e1-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="196e1-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="196e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="196e1-102">SYNOPSIS</span></span>
<span data-ttu-id="196e1-103">Erstellt eine Azure-ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="196e1-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="196e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="196e1-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="196e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="196e1-105">DESCRIPTION</span></span>
<span data-ttu-id="196e1-106">Mit dem Cmdlet **New-AzExpressRoutePortIdentity** wird ein lokales Azure ExpressRoutePort Identity-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="196e1-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="196e1-107">Verwenden Sie **New-AzExpressRoutePort** oder **AzExpressRoutePort** , um Sie zu Azure ExpressRoutePort zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="196e1-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="196e1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="196e1-108">EXAMPLES</span></span>

### <span data-ttu-id="196e1-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="196e1-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="196e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="196e1-110">PARAMETERS</span></span>

### <span data-ttu-id="196e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196e1-111">-DefaultProfile</span></span>
<span data-ttu-id="196e1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="196e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="196e1-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="196e1-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="196e1-114">Die Resourcen-ID der Benutzer zugewiesenen Identität, die ExpressRoutePort zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="196e1-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="196e1-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="196e1-115">-Confirm</span></span>
<span data-ttu-id="196e1-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="196e1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196e1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196e1-117">-WhatIf</span></span>
<span data-ttu-id="196e1-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="196e1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="196e1-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="196e1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196e1-120">CommonParameters</span></span>
<span data-ttu-id="196e1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196e1-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196e1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196e1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="196e1-123">INPUTS</span></span>

### <span data-ttu-id="196e1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="196e1-124">System.String</span></span>

## <span data-ttu-id="196e1-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="196e1-125">OUTPUTS</span></span>

### <span data-ttu-id="196e1-126">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="196e1-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="196e1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="196e1-127">NOTES</span></span>

## <span data-ttu-id="196e1-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="196e1-128">RELATED LINKS</span></span>
[<span data-ttu-id="196e1-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="196e1-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="196e1-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="196e1-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="196e1-131">Satz-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="196e1-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)