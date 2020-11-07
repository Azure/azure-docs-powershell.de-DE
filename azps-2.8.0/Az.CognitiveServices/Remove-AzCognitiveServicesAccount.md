---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: a0699722a4275855fc2203ac4a38ee5ebdee58f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652239"
---
# <span data-ttu-id="f8028-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f8028-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="f8028-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8028-102">SYNOPSIS</span></span>
<span data-ttu-id="f8028-103">Löscht ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="f8028-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="f8028-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8028-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8028-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8028-105">DESCRIPTION</span></span>
<span data-ttu-id="f8028-106">Das Cmdlet **Remove-AzCognitiveServicesAccount** löscht das angegebene Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="f8028-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="f8028-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8028-107">EXAMPLES</span></span>

### <span data-ttu-id="f8028-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8028-108">Example 1</span></span>
<span data-ttu-id="f8028-109">Dieser Befehl gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="f8028-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="f8028-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8028-110">PARAMETERS</span></span>

### <span data-ttu-id="f8028-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8028-111">-DefaultProfile</span></span>
<span data-ttu-id="f8028-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f8028-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8028-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f8028-113">-Force</span></span>
<span data-ttu-id="f8028-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f8028-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8028-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f8028-115">-Name</span></span>
<span data-ttu-id="f8028-116">Gibt den Namen des zu löschenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f8028-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="f8028-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8028-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8028-118">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f8028-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="f8028-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8028-119">-Confirm</span></span>
<span data-ttu-id="f8028-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8028-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8028-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8028-121">-WhatIf</span></span>
<span data-ttu-id="f8028-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8028-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8028-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8028-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8028-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8028-124">CommonParameters</span></span>
<span data-ttu-id="f8028-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8028-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8028-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8028-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8028-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8028-127">INPUTS</span></span>

### <span data-ttu-id="f8028-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f8028-128">System.String</span></span>

## <span data-ttu-id="f8028-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8028-129">OUTPUTS</span></span>

### <span data-ttu-id="f8028-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f8028-130">System.Void</span></span>

## <span data-ttu-id="f8028-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8028-131">NOTES</span></span>

## <span data-ttu-id="f8028-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8028-132">RELATED LINKS</span></span>

[<span data-ttu-id="f8028-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f8028-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f8028-134">Neu – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f8028-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f8028-135">Satz-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f8028-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


