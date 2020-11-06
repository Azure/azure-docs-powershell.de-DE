---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a182bed0e93492521e3ac46d5f0ed3e2d705394c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505229"
---
# <span data-ttu-id="b1231-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1231-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="b1231-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1231-102">SYNOPSIS</span></span>
<span data-ttu-id="b1231-103">Löscht ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="b1231-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1231-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1231-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1231-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1231-105">DESCRIPTION</span></span>
<span data-ttu-id="b1231-106">Das Cmdlet **Remove-AzureRmCognitiveServicesAccount** löscht das angegebene Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="b1231-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="b1231-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1231-107">EXAMPLES</span></span>

## <span data-ttu-id="b1231-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1231-108">PARAMETERS</span></span>

### <span data-ttu-id="b1231-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b1231-109">-Force</span></span>
<span data-ttu-id="b1231-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b1231-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1231-111">-Name</span><span class="sxs-lookup"><span data-stu-id="b1231-111">-Name</span></span>
<span data-ttu-id="b1231-112">Gibt den Namen des zu löschenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b1231-112">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1231-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1231-113">-ResourceGroupName</span></span>
<span data-ttu-id="b1231-114">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b1231-114">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="b1231-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1231-115">-Confirm</span></span>
<span data-ttu-id="b1231-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1231-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1231-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1231-117">-WhatIf</span></span>
<span data-ttu-id="b1231-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1231-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1231-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1231-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1231-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1231-120">-DefaultProfile</span></span>
<span data-ttu-id="b1231-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1231-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1231-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1231-122">CommonParameters</span></span>
<span data-ttu-id="b1231-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1231-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1231-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1231-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1231-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1231-125">INPUTS</span></span>

## <span data-ttu-id="b1231-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1231-126">OUTPUTS</span></span>

## <span data-ttu-id="b1231-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1231-127">NOTES</span></span>

## <span data-ttu-id="b1231-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1231-128">RELATED LINKS</span></span>

[<span data-ttu-id="b1231-129">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1231-129">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b1231-130">Neu – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1231-130">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b1231-131">Satz-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b1231-131">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


