---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 92e241703723d055d18083daae5fe424933f7c3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503901"
---
# <span data-ttu-id="4eeba-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4eeba-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4eeba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4eeba-102">SYNOPSIS</span></span>
<span data-ttu-id="4eeba-103">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4eeba-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eeba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eeba-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eeba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4eeba-105">DESCRIPTION</span></span>
<span data-ttu-id="4eeba-106">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4eeba-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="4eeba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4eeba-107">EXAMPLES</span></span>

### <span data-ttu-id="4eeba-108">Entfernt die Einstellungen des Facebook-Identitätsanbieters aus dem ApiManagement-Dienst</span><span class="sxs-lookup"><span data-stu-id="4eeba-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="4eeba-109">Löscht die Konfiguration in Bezug auf die Konfiguration des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="4eeba-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="4eeba-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eeba-110">PARAMETERS</span></span>

### <span data-ttu-id="4eeba-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4eeba-111">-Context</span></span>
<span data-ttu-id="4eeba-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4eeba-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4eeba-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4eeba-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eeba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eeba-114">-DefaultProfile</span></span>
<span data-ttu-id="4eeba-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4eeba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4eeba-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eeba-116">-PassThru</span></span>
<span data-ttu-id="4eeba-117">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="4eeba-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eeba-118">-Typ</span><span class="sxs-lookup"><span data-stu-id="4eeba-118">-Type</span></span>
<span data-ttu-id="4eeba-119">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="4eeba-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4eeba-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4eeba-120">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eeba-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4eeba-121">-Confirm</span></span>
<span data-ttu-id="4eeba-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4eeba-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eeba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eeba-123">-WhatIf</span></span>
<span data-ttu-id="4eeba-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4eeba-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4eeba-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4eeba-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eeba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eeba-126">CommonParameters</span></span>
<span data-ttu-id="4eeba-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eeba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eeba-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eeba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eeba-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4eeba-129">INPUTS</span></span>

### <span data-ttu-id="4eeba-130">Keine</span><span class="sxs-lookup"><span data-stu-id="4eeba-130">None</span></span>
<span data-ttu-id="4eeba-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4eeba-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4eeba-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4eeba-132">OUTPUTS</span></span>

### <span data-ttu-id="4eeba-133">bool</span><span class="sxs-lookup"><span data-stu-id="4eeba-133">bool</span></span>

## <span data-ttu-id="4eeba-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="4eeba-134">NOTES</span></span>

## <span data-ttu-id="4eeba-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4eeba-135">RELATED LINKS</span></span>

[<span data-ttu-id="4eeba-136">Neu – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4eeba-136">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4eeba-137">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4eeba-137">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4eeba-138">Satz-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4eeba-138">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

