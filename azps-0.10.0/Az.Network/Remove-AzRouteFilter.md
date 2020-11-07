---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 02f3e0a151fe8dc810e8530af88059371139f08c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843775"
---
# <span data-ttu-id="05395-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="05395-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="05395-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05395-102">SYNOPSIS</span></span>
<span data-ttu-id="05395-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="05395-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="05395-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05395-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05395-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05395-105">DESCRIPTION</span></span>
<span data-ttu-id="05395-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="05395-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="05395-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05395-107">EXAMPLES</span></span>

### <span data-ttu-id="05395-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05395-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="05395-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="05395-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="05395-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05395-110">PARAMETERS</span></span>

### <span data-ttu-id="05395-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05395-111">-DefaultProfile</span></span>
<span data-ttu-id="05395-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05395-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05395-113">-Force</span><span class="sxs-lookup"><span data-stu-id="05395-113">-Force</span></span>
<span data-ttu-id="05395-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="05395-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="05395-115">-Name</span><span class="sxs-lookup"><span data-stu-id="05395-115">-Name</span></span>
<span data-ttu-id="05395-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="05395-116">The resource name.</span></span>

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

### <span data-ttu-id="05395-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05395-117">-PassThru</span></span>
<span data-ttu-id="05395-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="05395-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="05395-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05395-119">-ResourceGroupName</span></span>
<span data-ttu-id="05395-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05395-120">The resource group name.</span></span>

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

### <span data-ttu-id="05395-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05395-121">-Confirm</span></span>
<span data-ttu-id="05395-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05395-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05395-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05395-123">-WhatIf</span></span>
<span data-ttu-id="05395-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05395-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05395-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05395-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05395-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05395-126">CommonParameters</span></span>
<span data-ttu-id="05395-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05395-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05395-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05395-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05395-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05395-129">INPUTS</span></span>

### <span data-ttu-id="05395-130">System. String</span><span class="sxs-lookup"><span data-stu-id="05395-130">System.String</span></span>

## <span data-ttu-id="05395-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05395-131">OUTPUTS</span></span>

### <span data-ttu-id="05395-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="05395-132">System.Object</span></span>

## <span data-ttu-id="05395-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="05395-133">NOTES</span></span>

## <span data-ttu-id="05395-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05395-134">RELATED LINKS</span></span>

