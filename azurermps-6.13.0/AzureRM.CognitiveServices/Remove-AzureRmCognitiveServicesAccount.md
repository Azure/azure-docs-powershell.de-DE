---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 2c8496af209cc72ebb6cb9a2ed40ae6033ce7268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503021"
---
# <span data-ttu-id="e558b-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e558b-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="e558b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e558b-102">SYNOPSIS</span></span>
<span data-ttu-id="e558b-103">Löscht ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="e558b-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e558b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e558b-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e558b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e558b-105">DESCRIPTION</span></span>
<span data-ttu-id="e558b-106">Das Cmdlet **Remove-AzureRmCognitiveServicesAccount** löscht das angegebene Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="e558b-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="e558b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e558b-107">EXAMPLES</span></span>

### <span data-ttu-id="e558b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e558b-108">Example 1</span></span>
<span data-ttu-id="e558b-109">Dieser Befehl gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="e558b-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="e558b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e558b-110">PARAMETERS</span></span>

### <span data-ttu-id="e558b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e558b-111">-DefaultProfile</span></span>
<span data-ttu-id="e558b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e558b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e558b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e558b-113">-Force</span></span>
<span data-ttu-id="e558b-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e558b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e558b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e558b-115">-Name</span></span>
<span data-ttu-id="e558b-116">Gibt den Namen des zu löschenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e558b-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="e558b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e558b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e558b-118">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e558b-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="e558b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e558b-119">-Confirm</span></span>
<span data-ttu-id="e558b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e558b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e558b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e558b-121">-WhatIf</span></span>
<span data-ttu-id="e558b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e558b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e558b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e558b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e558b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e558b-124">CommonParameters</span></span>
<span data-ttu-id="e558b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e558b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e558b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e558b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e558b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e558b-127">INPUTS</span></span>

### <span data-ttu-id="e558b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e558b-128">System.String</span></span>

## <span data-ttu-id="e558b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e558b-129">OUTPUTS</span></span>

### <span data-ttu-id="e558b-130">System. void</span><span class="sxs-lookup"><span data-stu-id="e558b-130">System.Void</span></span>

## <span data-ttu-id="e558b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e558b-131">NOTES</span></span>

## <span data-ttu-id="e558b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e558b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e558b-133">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e558b-133">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e558b-134">Neu – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e558b-134">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e558b-135">Satz-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e558b-135">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


