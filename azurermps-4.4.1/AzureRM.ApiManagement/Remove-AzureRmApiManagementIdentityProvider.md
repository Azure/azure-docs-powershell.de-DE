---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480002"
---
# <span data-ttu-id="44cbf-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="44cbf-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="44cbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="44cbf-103">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="44cbf-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44cbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44cbf-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44cbf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="44cbf-106">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="44cbf-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="44cbf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44cbf-107">EXAMPLES</span></span>

### <span data-ttu-id="44cbf-108">Entfernt die Einstellungen des Facebook-Identitätsanbieters aus dem ApiManagement-Dienst</span><span class="sxs-lookup"><span data-stu-id="44cbf-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="44cbf-109">Löscht die Konfiguration in Bezug auf die Konfiguration des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="44cbf-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="44cbf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="44cbf-110">PARAMETERS</span></span>

### <span data-ttu-id="44cbf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="44cbf-111">-Context</span></span>
<span data-ttu-id="44cbf-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="44cbf-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="44cbf-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44cbf-113">This parameter is required.</span></span>

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

### <span data-ttu-id="44cbf-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44cbf-114">-PassThru</span></span>
<span data-ttu-id="44cbf-115">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="44cbf-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="44cbf-116">-Typ</span><span class="sxs-lookup"><span data-stu-id="44cbf-116">-Type</span></span>
<span data-ttu-id="44cbf-117">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="44cbf-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="44cbf-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44cbf-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cbf-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44cbf-119">-Confirm</span></span>
<span data-ttu-id="44cbf-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44cbf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44cbf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44cbf-121">-WhatIf</span></span>
<span data-ttu-id="44cbf-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44cbf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44cbf-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44cbf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44cbf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cbf-124">-DefaultProfile</span></span>
<span data-ttu-id="44cbf-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44cbf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44cbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cbf-126">CommonParameters</span></span>
<span data-ttu-id="44cbf-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44cbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cbf-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44cbf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cbf-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44cbf-129">INPUTS</span></span>

## <span data-ttu-id="44cbf-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44cbf-130">OUTPUTS</span></span>

### <span data-ttu-id="44cbf-131">bool</span><span class="sxs-lookup"><span data-stu-id="44cbf-131">bool</span></span>

## <span data-ttu-id="44cbf-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="44cbf-132">NOTES</span></span>

## <span data-ttu-id="44cbf-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44cbf-133">RELATED LINKS</span></span>

[<span data-ttu-id="44cbf-134">Neu – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="44cbf-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="44cbf-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="44cbf-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="44cbf-136">Satz-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="44cbf-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

