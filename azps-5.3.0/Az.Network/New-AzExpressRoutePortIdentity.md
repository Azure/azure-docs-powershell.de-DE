---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379138"
---
# <span data-ttu-id="d2336-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2336-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="d2336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2336-102">SYNOPSIS</span></span>
<span data-ttu-id="d2336-103">Erstellt eine Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="d2336-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="d2336-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2336-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2336-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2336-105">DESCRIPTION</span></span>
<span data-ttu-id="d2336-106">Das **Cmdlet "New-AzExpressRoutePortIdentity"** erstellt ein lokales Azure ExpressRoutePort-Identitätsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d2336-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="d2336-107">Verwenden **Sie "New-AzExpressRoutePort"** oder **"Set-AzExpressRoutePort",** um es Azure ExpressRoutePort zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d2336-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="d2336-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2336-108">EXAMPLES</span></span>

### <span data-ttu-id="d2336-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2336-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="d2336-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2336-110">PARAMETERS</span></span>

### <span data-ttu-id="d2336-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2336-111">-DefaultProfile</span></span>
<span data-ttu-id="d2336-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2336-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2336-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="d2336-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="d2336-114">ResourceId der Benutzeridentität, die ExpressRoutePort zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2336-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="d2336-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2336-115">-Confirm</span></span>
<span data-ttu-id="d2336-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2336-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2336-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d2336-117">-WhatIf</span></span>
<span data-ttu-id="d2336-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2336-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2336-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2336-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2336-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2336-120">CommonParameters</span></span>
<span data-ttu-id="d2336-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2336-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2336-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2336-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2336-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2336-123">INPUTS</span></span>

### <span data-ttu-id="d2336-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d2336-124">System.String</span></span>

## <span data-ttu-id="d2336-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2336-125">OUTPUTS</span></span>

### <span data-ttu-id="d2336-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d2336-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="d2336-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2336-127">NOTES</span></span>

## <span data-ttu-id="d2336-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2336-128">RELATED LINKS</span></span>
[<span data-ttu-id="d2336-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2336-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="d2336-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2336-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="d2336-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2336-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)