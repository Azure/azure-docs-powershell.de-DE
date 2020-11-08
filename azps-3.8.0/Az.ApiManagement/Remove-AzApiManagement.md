---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996908"
---
# <span data-ttu-id="455df-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="455df-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="455df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="455df-102">SYNOPSIS</span></span>
<span data-ttu-id="455df-103">Entfernt einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="455df-103">Removes an API Management service.</span></span>

## <span data-ttu-id="455df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="455df-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="455df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="455df-105">DESCRIPTION</span></span>
<span data-ttu-id="455df-106">Mit dem Cmdlet **Remove-AzApiManagement** wird ein Azure API-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="455df-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="455df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="455df-107">EXAMPLES</span></span>

### <span data-ttu-id="455df-108">Beispiel 1: Entfernen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="455df-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="455df-109">Mit diesem Befehl wird der API-Verwaltungsdienst mit dem Namen ContosoApi entfernt.</span><span class="sxs-lookup"><span data-stu-id="455df-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="455df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="455df-110">PARAMETERS</span></span>

### <span data-ttu-id="455df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455df-111">-DefaultProfile</span></span>
<span data-ttu-id="455df-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="455df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="455df-113">-Name</span><span class="sxs-lookup"><span data-stu-id="455df-113">-Name</span></span>
<span data-ttu-id="455df-114">Gibt den Namen der API-Verwaltungs Bereitstellung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="455df-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="455df-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="455df-115">-PassThru</span></span>
<span data-ttu-id="455df-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="455df-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="455df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455df-117">-ResourceGroupName</span></span>
<span data-ttu-id="455df-118">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="455df-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="455df-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="455df-119">-Confirm</span></span>
<span data-ttu-id="455df-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="455df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="455df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="455df-121">-WhatIf</span></span>
<span data-ttu-id="455df-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="455df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="455df-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="455df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="455df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455df-124">CommonParameters</span></span>
<span data-ttu-id="455df-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="455df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455df-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="455df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455df-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="455df-127">INPUTS</span></span>

### <span data-ttu-id="455df-128">System. String</span><span class="sxs-lookup"><span data-stu-id="455df-128">System.String</span></span>

## <span data-ttu-id="455df-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="455df-129">OUTPUTS</span></span>

### <span data-ttu-id="455df-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="455df-130">System.Boolean</span></span>

## <span data-ttu-id="455df-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="455df-131">NOTES</span></span>

## <span data-ttu-id="455df-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="455df-132">RELATED LINKS</span></span>

[<span data-ttu-id="455df-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="455df-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="455df-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="455df-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="455df-135">Neu – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="455df-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="455df-136">Wiederherstellen – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="455df-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


