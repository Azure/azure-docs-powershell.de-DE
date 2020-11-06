---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480010"
---
# <span data-ttu-id="09781-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09781-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="09781-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09781-102">SYNOPSIS</span></span>
<span data-ttu-id="09781-103">Entfernt ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="09781-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09781-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09781-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09781-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09781-105">DESCRIPTION</span></span>
<span data-ttu-id="09781-106">Entfernt ein vom Bezeichner angegebenes Back-End aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="09781-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="09781-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09781-107">EXAMPLES</span></span>

### <span data-ttu-id="09781-108">Beispiel 1: Entfernen des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="09781-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="09781-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="09781-109">PARAMETERS</span></span>

### <span data-ttu-id="09781-110">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="09781-110">-BackendId</span></span>
<span data-ttu-id="09781-111">Bezeichner des vorhandenen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="09781-111">Identifier of existing backend.</span></span>
<span data-ttu-id="09781-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09781-112">This parameter is required.</span></span>

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

### <span data-ttu-id="09781-113">-Context</span><span class="sxs-lookup"><span data-stu-id="09781-113">-Context</span></span>
<span data-ttu-id="09781-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="09781-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="09781-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09781-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09781-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09781-116">-PassThru</span></span>
<span data-ttu-id="09781-117">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="09781-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="09781-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="09781-118">This parameter is optional.</span></span>
<span data-ttu-id="09781-119">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="09781-119">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09781-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09781-120">-Confirm</span></span>
<span data-ttu-id="09781-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09781-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09781-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09781-122">-WhatIf</span></span>
<span data-ttu-id="09781-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09781-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09781-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09781-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09781-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09781-125">-DefaultProfile</span></span>
<span data-ttu-id="09781-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09781-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09781-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09781-127">CommonParameters</span></span>
<span data-ttu-id="09781-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09781-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09781-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09781-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09781-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09781-130">INPUTS</span></span>

## <span data-ttu-id="09781-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09781-131">OUTPUTS</span></span>

### <span data-ttu-id="09781-132">bool</span><span class="sxs-lookup"><span data-stu-id="09781-132">bool</span></span>

## <span data-ttu-id="09781-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="09781-133">NOTES</span></span>

## <span data-ttu-id="09781-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09781-134">RELATED LINKS</span></span>

[<span data-ttu-id="09781-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09781-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="09781-136">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09781-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="09781-137">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="09781-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="09781-138">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="09781-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="09781-139">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09781-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
