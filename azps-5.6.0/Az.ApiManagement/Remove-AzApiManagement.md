---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: daa4169ed077003d2ceb773e2e085e72fb6d1ec8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922192"
---
# <span data-ttu-id="f0057-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0057-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="f0057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0057-102">SYNOPSIS</span></span>
<span data-ttu-id="f0057-103">Entfernt einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="f0057-103">Removes an API Management service.</span></span>

## <span data-ttu-id="f0057-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0057-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0057-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0057-105">DESCRIPTION</span></span>
<span data-ttu-id="f0057-106">Das **Cmdlet Remove-AzApiManagement** entfernt einen Azure-API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="f0057-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="f0057-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0057-107">EXAMPLES</span></span>

### <span data-ttu-id="f0057-108">Beispiel 1: Entfernen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="f0057-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="f0057-109">Mit diesem Befehl wird der API-Verwaltungsdienst namens ContosoApi entfernt.</span><span class="sxs-lookup"><span data-stu-id="f0057-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="f0057-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0057-110">PARAMETERS</span></span>

### <span data-ttu-id="f0057-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0057-111">-DefaultProfile</span></span>
<span data-ttu-id="f0057-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0057-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0057-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f0057-113">-Name</span></span>
<span data-ttu-id="f0057-114">Gibt den Namen der API-Verwaltungsbereitstellung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f0057-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0057-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0057-115">-PassThru</span></span>
<span data-ttu-id="f0057-116">Gibt an, dass dieses Cmdlet einen Wert von $True, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="f0057-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="f0057-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0057-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0057-118">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungsbereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f0057-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="f0057-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0057-119">-Confirm</span></span>
<span data-ttu-id="f0057-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0057-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0057-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0057-121">-WhatIf</span></span>
<span data-ttu-id="f0057-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0057-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0057-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0057-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0057-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0057-124">CommonParameters</span></span>
<span data-ttu-id="f0057-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0057-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0057-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0057-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0057-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0057-127">INPUTS</span></span>

### <span data-ttu-id="f0057-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f0057-128">System.String</span></span>

## <span data-ttu-id="f0057-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0057-129">OUTPUTS</span></span>

### <span data-ttu-id="f0057-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0057-130">System.Boolean</span></span>

## <span data-ttu-id="f0057-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0057-131">NOTES</span></span>

## <span data-ttu-id="f0057-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0057-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0057-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0057-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="f0057-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0057-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="f0057-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0057-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f0057-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0057-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


