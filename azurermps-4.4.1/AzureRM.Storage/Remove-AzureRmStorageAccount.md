---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: ba63794844420accf2e5e664a43f74b2578c780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662882"
---
# <span data-ttu-id="8051d-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8051d-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="8051d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8051d-102">SYNOPSIS</span></span>
<span data-ttu-id="8051d-103">Entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="8051d-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8051d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8051d-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8051d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8051d-105">DESCRIPTION</span></span>
<span data-ttu-id="8051d-106">Das Cmdlet **Remove-AzureRmStorageAccount** entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="8051d-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="8051d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8051d-107">EXAMPLES</span></span>

### <span data-ttu-id="8051d-108">Beispiel 1: Entfernen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8051d-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="8051d-109">Mit diesem Befehl wird das angegebene Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="8051d-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="8051d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8051d-110">PARAMETERS</span></span>

### <span data-ttu-id="8051d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8051d-111">-Force</span></span>
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

### <span data-ttu-id="8051d-112">-Name</span><span class="sxs-lookup"><span data-stu-id="8051d-112">-Name</span></span>
<span data-ttu-id="8051d-113">Gibt den Namen des zu entfernenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="8051d-113">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8051d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8051d-114">-ResourceGroupName</span></span>
<span data-ttu-id="8051d-115">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="8051d-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="8051d-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8051d-116">-Confirm</span></span>
<span data-ttu-id="8051d-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8051d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8051d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8051d-118">-WhatIf</span></span>
<span data-ttu-id="8051d-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8051d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8051d-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8051d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8051d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8051d-121">-DefaultProfile</span></span>
<span data-ttu-id="8051d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8051d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8051d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8051d-123">CommonParameters</span></span>
<span data-ttu-id="8051d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8051d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8051d-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8051d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8051d-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8051d-126">INPUTS</span></span>

## <span data-ttu-id="8051d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8051d-127">OUTPUTS</span></span>

## <span data-ttu-id="8051d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8051d-128">NOTES</span></span>

## <span data-ttu-id="8051d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8051d-129">RELATED LINKS</span></span>

[<span data-ttu-id="8051d-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8051d-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="8051d-131">Neu – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8051d-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="8051d-132">Satz-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8051d-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


