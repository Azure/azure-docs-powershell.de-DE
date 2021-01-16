---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296273"
---
# <span data-ttu-id="cfd78-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="cfd78-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="cfd78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfd78-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd78-103">Löscht einen IotHub.</span><span class="sxs-lookup"><span data-stu-id="cfd78-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="cfd78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfd78-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd78-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfd78-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd78-106">Löscht einen IotHub.</span><span class="sxs-lookup"><span data-stu-id="cfd78-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="cfd78-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cfd78-107">EXAMPLES</span></span>

### <span data-ttu-id="cfd78-108">Beispiel 1: Entfernen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="cfd78-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="cfd78-109">Entfernt einen IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cfd78-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="cfd78-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfd78-110">PARAMETERS</span></span>

### <span data-ttu-id="cfd78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd78-111">-DefaultProfile</span></span>
<span data-ttu-id="cfd78-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cfd78-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfd78-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cfd78-113">-Name</span></span>
<span data-ttu-id="cfd78-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="cfd78-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd78-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd78-115">-ResourceGroupName</span></span>
<span data-ttu-id="cfd78-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="cfd78-116">Resource Group Name</span></span>

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

### <span data-ttu-id="cfd78-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfd78-117">-Confirm</span></span>
<span data-ttu-id="cfd78-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfd78-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd78-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cfd78-119">-WhatIf</span></span>
<span data-ttu-id="cfd78-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfd78-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfd78-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfd78-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd78-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd78-122">CommonParameters</span></span>
<span data-ttu-id="cfd78-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd78-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd78-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd78-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd78-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cfd78-125">INPUTS</span></span>

### <span data-ttu-id="cfd78-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cfd78-126">System.String</span></span>

## <span data-ttu-id="cfd78-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cfd78-127">OUTPUTS</span></span>

### <span data-ttu-id="cfd78-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="cfd78-128">System.Void</span></span>

## <span data-ttu-id="cfd78-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cfd78-129">NOTES</span></span>

## <span data-ttu-id="cfd78-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cfd78-130">RELATED LINKS</span></span>
